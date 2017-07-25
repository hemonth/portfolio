+++
date = "2017-07-20T12:00:00"
draft = false
tags = ["Angular4", "Material Design"]
title = "Angular 4 material design and animations introduction"
summary = """
How to install Angular 4 Material design into your project
"""

[header]
image = "building-a-lightning-app-with-angular-material-design.jpg"
# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

**Step 1: Install it through command line:**<br>

  ```angular
  npm install --save @angular/material @angular/animations.
  ```

**Step 2: Add below import statements in app.module**<br>

  ```python
  import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
  import { MdButtonModule, MdCardModule, MdMenuModule, MdToolbarModule, MdIconModule} from '@angular/material';
  @NgModule({
  imports: [
   BrowserAnimationsModule,
   MdButtonModule,
   MdCardModule,
   MdMenuModule,
   MdToolbarModule,
   MdIconModule
  ],
  })
  ```

  Alternatively, you can create a separate NgModule that imports all of the Angular Material components that you will use in your application. You can then include this module wherever you'd like to use the components.

```python
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { MdButtonModule, MdCardModule, MdMenuModule, MdToolbarModule, MdIconModule} from '@angular/material';

@NgModule({
    imports: [
    BrowserAnimationsModule,
    MdButtonModule,
    MdCardModule,
    MdMenuModule,
    MdToolbarModule,
    MdIconModule
  ],
  exports: [
    BrowserAnimationsModule,
    MdButtonModule,
    MdCardModule,
    MdMenuModule,
    MdToolbarModule,
    MdIconModule
  ],
})
export class MyOwnCustomMaterialModule { }
```

Whichever approach you use, be sure to import the Angular Material modules after Angular's BrowserModule, as the import order matters for NgModules.

**Step 3: Include a theme**<br> Including a theme is **required** to apply all of the core and theme styles to your application.<br>
  To get started with a prebuilt theme, include one of Angular Material's prebuilt themes globally in your application. If you're using the Angular CLI, you can add this to your `styles.css`:

  ```javascript
  @import "~@angular/material/prebuilt-themes/indigo-pink.css";
  ```

  If you are not using the Angular CLI, you can include a prebuilt theme via a element in your `index.html`.

**Step 4: Add Material Icons**<br> If you want to use the `md-icon` component with the official Material Design Icons, load the icon font in your `index.html`.

  ```javascript
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  ```

  For more information on using Material Icons, check out the [Material Icons Guide](https://google.github.io/material-design-icons/).
