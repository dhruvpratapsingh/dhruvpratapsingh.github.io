---
title: "3001: Angular Amplify - Install Prettier & Husky"
---

In this tutorial we will be installing Prettier & Husky to help us with code formatting. When we started migrating to Angular we had a lot to figure out and wanted to avoid wasting time on formatting changes. So we researched a bit and found two fantastic libraries. After 10k+ commits we still haven't asked anyone to fix formatting of their code in the code review channel, thanks to these amazing duos.

# [Prettier](https://prettier.io/){:target="_blank"}

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

<!-- Image for Prettier in package.json -->
<!-- <p align="center">
  <img src="./../../../../assets/images/angular/scripts-prettier.png"/>
</p> -->


# [Husky](https://www.npmjs.com/package/husky){:target="_blank"}
