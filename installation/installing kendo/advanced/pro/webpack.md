# Webpack

1. Run `npm install --save git+https://my.telerik.identity%40example.com:mypassword@bower.telerik.com/npm-kendo-ui.git`. Replace `my.telerik.identity%40example.com` with your telerik e-mail (url encoded) and `mypassword` with your password 
<br><br>
**WARNING: If you --save or --save-dev then your password will be visible in package.json**
<br><br>
2. Add the following lines to the `head` section of `index.html`:
    ```html
    <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.common.core.min.css">
    <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.default.min.css">
    ```
3. Add the following import to `main.js`:
  ```javascript
  import "kendo";
  ```