# Webpack

1. Follow [these instructions](http://docs.telerik.com/kendo-ui/intro/installation/npm#kendo-ui-professional) which tells you to run `npm install --save git+https://my.telerik.identity%40example.com:mypassword@bower.telerik.com/npm-kendo-ui.git`. Replace `my.telerik.identity%40example.com` with your telerik e-mail (`%40` = `@`) and `mypassword` with your password
2. Add the following lines to the `head` section of `index.html`:
    ```html
    <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.common.core.min.css">
    <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.default.min.css">
    ```
3. Add the following import to `main.js`:
  ```javascript
  import "kendo-ui-core";
  ```