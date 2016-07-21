# Downloaded ZIP

1. Download the Kendo ZIP from Telerik's website ([instructions](../../simple/kendo_all_min_js)).
1. Create a `kendo-sdk` folder in the root (at the same level as the src folder)
![img](http://i.imgur.com/HefXpuN.png)
3. Extract the `js` and `styles` folder from the ZIP into the `kendo-sdk` folder
4. Open `config.js` and add two path mappings:

    ```
    paths: {
      "*": "dist/*",
      "github:*": "jspm_packages/github/*",
      "npm:*": "jspm_packages/npm/*",
      "kendo.*": "kendo-sdk/js/kendo.*.js",        <----
      "kendo-ui/*": "kendo-sdk/*"                 <----
    },
    "map": {
      "aurelia-bootstrapper": "npm:aurelia-bootstrapper@1.0.0-beta.1",
      "aurelia-fetch-client": "npm:aurelia-fetch-client@1.0.0-beta.1",
      "aurelia-framework": "npm:aurelia-framework@1.0.0-beta.1.0.2"
    }
    ```

  **Note:** you may have to update the version of Kendo when adding these mappings.  
  **Note:** old versions of Kendo require a jquery.min map that is the equivalent of the jquery map: "jquery.min": "github:components/jquery@2.1.4"

5. Install the aurelia-kendoui-bridge and the css plugin
`jspm install css jquery aurelia-kendoui-bridge`

6. Register the aurelia-kendoui-bridge plugin
Now we're going to register the plugin with Aurelia in your "main.js" or equivalent. The configuration function will be passed a builder object that you can use to configure which Kendo controls you wish to use. You can use all controls in Kendo UI Pro by calling the "pro()" method

    ```
    export function configure(aurelia) {
      aurelia.use
        .standardConfiguration()
        .developmentLogging()
        .plugin('aurelia-kendoui-bridge', (kendo) => kendo.pro());

      aurelia.start().then(a => a.setRoot());
    }
    ```

7. Now let's open up "app.html" and load Kendo's CSS files

    ```
    <require from="kendo-ui/styles/kendo.common.min.css!"></require>
    <require from="kendo-ui/styles/kendo.bootstrap.min.css!"></require>
    ```

### You are done!
It is now possible to drop some custom-elements into your DOM. See the other pages on this website for detailed information on how to do this.

**We recommend that you read [these instructions](https://aurelia-ui-toolkits.gitbooks.io/kendoui-bridge-docs/content/what_you_need_to_know.html) in order to get started**

**Loading all wrappers too slow? Lazy loading of wrappers is also possible: [instructions](#/help/docs/app_developers_notes/3._lazy_loading_wrappers)**
