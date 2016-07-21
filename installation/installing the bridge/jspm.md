# JSPM

1. run `jspm install aurelia-kendoui-bridge`
2. open main.js and register the plugin:
    ```
    export function configure(aurelia) {
      aurelia.use
        .standardConfiguration()
        .developmentLogging()
        .plugin('aurelia-kendoui-bridge');

      aurelia.start().then(a => a.setRoot());
    }
    ```