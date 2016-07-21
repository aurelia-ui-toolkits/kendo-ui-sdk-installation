# JSPM


1. Install KendoUI Core by issuing the command:
`jspm install jquery css kendo-ui`

2. Open `config.js` and add this path mapping:

  ```
  paths: {
    "*": "dist/*",
    "github:*": "jspm_packages/github/*",
    "npm:*": "jspm_packages/npm/*",
    "kendo.*": "jspm_packages/github/kendo-labs/bower-kendo-ui@2016.2.714/js/kendo.*.js"    <----
  },
  "map": {
    "aurelia-bootstrapper": "npm:aurelia-bootstrapper@1.0.0-beta.1",
    "aurelia-fetch-client": "npm:aurelia-fetch-client@1.0.0-beta.1",
    "aurelia-framework": "npm:aurelia-framework@1.0.0-beta.1.0.2"
  }
  ```

  **Note:** Make sure that you reference the correct version of Kendo in the `kendo.*` map.  
  **Note:** old versions of Kendo require a jquery.min map that is the equivalent of the jquery map: "jquery.min": "github:components/jquery@2.1.4"

3. Now let's open up "app.html" and load Kendo's CSS files

```
<require from="kendo-ui/styles/kendo.common.min.css!"></require>
<require from="kendo-ui/styles/kendo.bootstrap.min.css!"></require>
```