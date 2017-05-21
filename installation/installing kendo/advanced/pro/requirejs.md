# Aurelia-CLI

1. Follow [these instructions](http://docs.telerik.com/kendo-ui/intro/installation/npm#kendo-ui-professional) to install Kendo-UI
2. Install jquery: `npm install jquery --save`
3. Add the following stylesheets to the `head` section of `index.html:
```html
    <link rel="stylesheet" href="node_modules/@progress/kendo-ui/css/web/kendo.common.core.min.css">
    <link rel="stylesheet" href="node_modules/@progress/kendo-ui/css/web/kendo.default.min.css">
```
4. Open `aurelia_project/aurelia.json` and append the following configuration to the `dependencies` section of the `vendor-bundle`:
```json
  "jquery",
  {
    "name": "kendo",
    "path": "../node_modules/@progress/kendo-ui/",
    "resources": [
      "js/kendo.button.js"
    ]
  },
```

Everything in the resources property will be added to the bundle. If you do not declare the controls that you use, RequireJS will fetch them at runtime, which might cause issues during deployment

5.  Kendo controls can be loaded as follows:
  ```javascript
import 'kendo/js/kendo.datepicker';
  ```

6. **Warning**: The error you get during the tracing process of `au run` is expected and harmless. More can be read in [this issue](https://github.com/aurelia-ui-toolkits/aurelia-kendoui-bridge/issues/660)
