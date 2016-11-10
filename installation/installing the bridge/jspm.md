### [JSPM](http://jspm.io/)

<p align=center>
  <img src="https://cloud.githubusercontent.com/assets/2712405/15519572/1b2da524-21d0-11e6-8d69-a55bd36d1605.png"></img>
 <br><br>
</p>

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
    
### Important
It is strongly recommended to continue with the [getting started](./getting-started.md) page