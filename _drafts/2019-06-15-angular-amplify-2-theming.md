---
title: "3002: Angular Amplify - Theming Angular Material Components"
---

**Summary:**
1. Install Angular Material, Angular CDK and Angular Animations.
2. Configure Animations.
3. Add Material Icons.
4. Include Material Theme.
5. Customize Material Theme.

## Install Angular Material
Let's install Angular Material, Angular CDK, HammerJS and Angular Animations.

```
npm install --save @angular/material @angular/cdk @angular/animations
```

Note that HammerJs is for gesture support.

## Configure Animations
Since angular material depends heavily on animations, let us configure that.

```javascript
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class AppModule { }
```

## Add Material icons
Include material icons in your index.html

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Levanteq</title>
  <base href="/">

  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
</head>
<body>
  <app-root></app-root>
</body>
</html>
```

## Include Material Theme
Add the line below to your styles.scss.

```javascript
@import "~@angular/material/prebuilt-themes/indigo-pink.css";
```

## Customize Material themes
Finally! Time for fun.

[Tools](https://material.io/tools/): You can checkout various tools available to help you with component design.

We will be using [Glitch](https://glitch.com/~material-theme-builder) for our we component design and testing.

There are plugins for Sketch to test and play with the material theme to generate components for you. But since they need license, I preferred to use Glitch for the purpose of this tutorial. It can be slow sometimes but it also does a lot behind the scenes.

Let's [Create New Theme](https://glitch.com/edit/#!/remix/material-theme-builder) on Glitch.

### Color Palette
Visit [Material Color Palette](http://mcg.mbitson.com) to get the color palette for your primary and secondary colors. You can click on notepad icon to generate color palette for you app by further selecting Angular Js 2(Material 2 option). Paste the color palette in you app-theme.scss file.

{% include ads.html %}
