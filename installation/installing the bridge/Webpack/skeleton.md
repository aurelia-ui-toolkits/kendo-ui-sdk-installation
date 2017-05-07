### Installing the bridge

1. `npm install aurelia-kendoui-bridge --save`
2. in `src/main.js` load the plugin using `.plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'))`:
   ```  
   aurelia.use
    .standardConfiguration()
    .plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'))
    .developmentLogging();
   ```
3. in webpack.config.js add an entry for the aurelia-kendoui-bridge:
   ```
   entry: {
    app: ['aurelia-bootstrapper'],
    vendor: ['bluebird', 'jquery', 'bootstrap', 'aurelia-kendoui-bridge'],
   },
   ```
4. That's it!