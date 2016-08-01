# Webpack

1. Install kendo-core and jquery: `npm install kendo-ui-core jquery --save`
2. Add the following stylesheets to the `head` section of `index.html:
  ```html
    <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.common.core.min.css">
    <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.default.min.css">
  ```
3. Add the following import to `main.js`:
  ```javascript
  import "kendo-ui-core";
  ```