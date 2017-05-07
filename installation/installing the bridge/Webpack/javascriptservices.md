### Installing the bridge
1. `npm install aurelia-kendoui-bridge --save`
2. in `ClientApp/app/boot.ts` add `.plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'));` like so:
   ```
   aurelia.use.standardConfiguration()
     .plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'));
   ```
3. in `webpack.config.js` add the following statement to the `entry.vendor` section: `'aurelia-kendoui-bridge'`

   ```
    entry: {
        vendor: [
            'aurelia-event-aggregator',
            'aurelia-fetch-client',
            'aurelia-framework',
            'aurelia-history-browser',
            'aurelia-logging-console',
            'aurelia-pal-browser',
            'aurelia-polyfills',
            'aurelia-route-recognizer',
            'aurelia-router',
            'aurelia-templating-binding',
            'aurelia-templating-resources',
            'aurelia-templating-router',
            'bootstrap',
            'bootstrap/dist/css/bootstrap.css',
            'jquery',
            'aurelia-kendoui-bridge'
        ],
    },
   ```

4. That's it!

