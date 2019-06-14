---
title: "3001: Angular Amplify - Install Prettier & Husky"
---

In this tutorial we will be installing Prettier & Husky to help us with code formatting. When we started migrating to Angular we had a lot to figure out and wanted to avoid wasting time on formatting changes. So we researched a bit and found two fantastic libraries. After 10k+ commits we still haven't asked anyone to fix formatting of their code in the code review channel, thanks to these amazing duos.

# [Prettier](https://prettier.io/)

Prettier is an opinionated code formatter which we will be using to format our Typescript code. It parses the code and formats based on the pre-defined rules. We will start with adding Prettier to our project and later we will override some of the rules to fit our needs.

```
# Install Prettier as dev-dependency
npm install prettier -D
```

Once installed successfully, add lines below to the scripts property in your project's `package.json` file.

```
"prettier:base": "prettier --parser typescript --single-quote",
"prettier:check": "npm run prettier:base -- --list-different \"src/**/*.{ts,tsx}\"",
"prettier:write": "npm run prettier:base -- --write \"src/**/*.{ts,tsx}\""
```
Would be placed something like this.

```javascript
"scripts": {
  "ng": "ng",
  "start": "ng serve",
  "build": "ng build",
  "test": "ng test",
  "lint": "ng lint",
  "e2e": "ng e2e",
  "prettier:base": "prettier --parser typescript --single-quote",
  "prettier:check": "npm run prettier:base -- --list-different \"src/**/*.{ts,tsx}\"",
  "prettier:write": "npm run prettier:base -- --write \"src/**/*.{ts,tsx}\""
},
```

Test it:

Open your app.component.ts

Unformatted:
```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  title = 'levanteq';

  testPrettier(reallyLongArg, omgSoManyParameters, IShouldRefactorThis, isThereSeriouslyAnotherOne) {
                            const isTooFarFromBoundary = true;
}
}
```
# Run prettier
npm run prettier:write

Formatted:
```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  title = 'levanteq';

  testPrettier(
    reallyLongArg,
    omgSoManyParameters,
    IShouldRefactorThis,
    isThereSeriouslyAnotherOne
  ) {
    const isTooFarFromBoundary = true;
  }
}
```

It's magical!!

If you want to override a style you can do it by simply adding `.prettierrc` file parallel to package.json file. Here is a sample from our app.

```javascript
{
  "printWidth": 120,
  "singleQuote": true,
  "useTabs": false,
  "tabWidth": 2,
  "semi": true,
  "bracketSpacing": true
}
```

# [Husky](https://www.npmjs.com/package/husky){:target="_blank"}

Husky provides us with a pre-commit hook so we don't have to do this manually. Everytime you commit, it will format the code for you by running Prettier.

```
# Install husky as a dev-dependency
npm install husky -D
```

Create a file named `.huskyrc` and add it parallel to package.json file. Add below to it.

```javascript
{
  "hooks": {
    "pre-commit": "npm run prettier:write"
  }
}
```

You can test that now when you commit your code
