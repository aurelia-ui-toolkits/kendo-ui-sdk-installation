# Aurelia-CLI

1. Install kendo-core and jquery: `npm install kendo-ui-core jquery --save`
<br><br>
2. Add the following stylesheets to the `head` section of `index.html:
```html
  <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.common.core.min.css">
  <link rel="stylesheet" href="node_modules/kendo-ui-core/css/web/kendo.default.min.css">
```
<br><br>
3. Open `aurelia_project/aurelia.json` and append the following configuration to the `dependencies` section of the `vendor-bundle`:
```json
  "jquery",
  {
    "name": "kendo-ui-core",
    "path": "../node_modules/kendo-ui-core/"
  }
```
<br><br>
4. Kendo controls can be loaded as follows:
```javascript
import * as $ from 'jquery';
import 'kendo-ui-core/js/kendo.button';
```
<br><br>
***
***

