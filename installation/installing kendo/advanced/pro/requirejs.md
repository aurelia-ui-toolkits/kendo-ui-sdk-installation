# Aurelia-CLI


1. Run `npm install git+https://my.telerik.identity%40example.com:mypassword@bower.telerik.com/npm-kendo-ui.git`. Replace `my.telerik.identity%40example.com` with your telerik e-mail (url encoded) and `mypassword` with your password
<br><br>
**WARNING: If you --save or --save-dev then your password will be visible in package.json**
<br><br>
2. Install jquery: `npm install jquery --save`
3. Add the following stylesheets to the `head` section of `index.html:
```html
  <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.common.core.min.css">
  <link rel="stylesheet" href="node_modules/kendo/css/web/kendo.default.min.css">
```
4. Open `aurelia_project/aurelia.json` and append the following configuration to the `dependencies` section of the `vendor-bundle`:
```json
  "jquery",
  {
    "name": "kendo",
    "path": "../node_modules/kendo/"
  }
```
5.  Kendo controls can be loaded as follows:
  ```javascript
  import * as $ from 'jquery';
  import 'kendo/js/kendo.button';
  ```

