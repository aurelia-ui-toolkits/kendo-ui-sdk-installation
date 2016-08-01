# Aurelia-CLI
1. `npm install aurelia-kendoui-bridge --save`
<br><br>
2. Open `aureli_project/aurelia.json` and append the following to the `dependencies` section of the `vendor-bundle`:

  ```json
{
    "name": "aurelia-kendoui-bridge",
    "path": "../node_modules/aurelia-kendoui-bridge/dist/amd",
    "main": "index"
}
```

3. Open `main.js` and register the plugin

  ```javascript
  aurelia.use
    .standardConfiguration()
    .feature('resources')
    .plugin('aurelia-kendoui-bridge');
```

