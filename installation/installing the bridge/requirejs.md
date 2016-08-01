# Aurelia-CLI
1. `npm install aurelia-kendoui-bridge --save`
<br><br>
2. Open `aurelia_project/aurelia.json` and append the following to the `dependencies` section of the `vendor-bundle`:

  ```json
{
    "name": "aurelia-kendoui-bridge",
    "path": "../node_modules/aurelia-kendoui-bridge/dist/amd",
    "main": "index"
}
```

3. While still in the `aurelia.json` file, change the `stub` property of the `text` plugin to `false`:
   ```json
   {
    "name": "text",
    "extensions": [
      ".html",
      ".css"
    ],
    "stub": false
  }
  ```

3. Open `main.js` and register the plugin

  ```javascript
  aurelia.use
    .standardConfiguration()
    .feature('resources')
    .plugin('aurelia-kendoui-bridge');
```

### Important
It is strongly recommended to continue with the [getting started](./getting-started.md) page

