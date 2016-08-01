# Webpack

1. Install kendo-core and jquery: `npm install kendo-ui-core jquery --save`
2. Add the following stylesheets to the `head` section of `index.html:
```html
  <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.common.core.min.css">
  <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.default.min.css">
```
3. Open `aurelia_project/aurelia.json` and append the following configuration to the `dependencies` section of the `vendor-bundle`:
```json
  "jquery",
  {
    "name": "kendo-ui-core",
    "path": "../node_modules/kendo-ui-core/"
  }
```

Loading Kendo controls can be done as follows:
```javascript
import * as $ from 'jquery';
import 'kendo-ui-core/js/kendo.button';
```