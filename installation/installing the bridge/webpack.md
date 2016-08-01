# Webpack
1. Install the bridge: `npm install aurelia-kendoui-bridge --save`
2. Open `webpack.config.js` and add the following to the `coreBundles`
```javascript
  kendo: [
    'aurelia-kendoui-bridge'
  ]
```
3. While still in `webpack.config.js`, add the following line to `baseConfig`'s entry property:
```
  'aurelia-kendoui-bridge': ['aurelia-kendoui-bridge']
```
4. Now you can load wrappers of the aurelia-kendoui-bridge via `<require>` and they will be added to the webpack bundle
```html
  <require from="aurelia-kendoui-bridge/grid/grid"></require>
  <require from="aurelia-kendoui-bridge/grid/col"></require>
```
5. open main.js and register the plugin:
    ```
    export function configure(aurelia) {
      aurelia.use
        .standardConfiguration()
        .developmentLogging()
        .plugin('aurelia-kendoui-bridge');

      aurelia.start().then(a => a.setRoot());
    }
    ```