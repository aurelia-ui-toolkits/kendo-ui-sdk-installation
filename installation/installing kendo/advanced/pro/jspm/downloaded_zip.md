# _This page is deprecated_

(see **[general comments](./general-comments.html)** for explanation)

***
***
***


# Downloaded ZIP

1. Install the css plugin of JSPM: `jspm install css`
<br><br>
2. Download the Kendo ZIP from Telerik's website ([instructions](../../simple/kendo_all_min_js)).
<br><br> 
3. Create a `kendo-sdk` folder in the root (at the same level as the src folder)
![img](http://i.imgur.com/HefXpuN.png)
<br><br>
4. Extract the `js` and `styles` folder from the ZIP into the `kendo-sdk` folder
<br><br>
5. Open `config.js` and add two path mappings:

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

  **Note:** old versions of Kendo require a jquery.min map that is the equivalent of the jquery map: "jquery.min": "github:components/jquery@2.1.4"
<br><br>
6. Now let's open up `app.html` and load Kendo's CSS files

    ```
    <require from="kendo-sdk/styles/kendo.common.min.css!"></require>
    <require from="kendo-sdk/styles/kendo.bootstrap.min.css!"></require>
    ```
<br><br>
***
***