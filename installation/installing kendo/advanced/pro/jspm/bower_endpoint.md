# _This page is deprecated_

(see **[general comments](./general-comments.html)** for explanation)

***
***
***



# Bower endpoint

1. Install the JSPM git endpoint plugin by issuing the command:
`npm install jspm-git --save-dev`
<br>

2. Register the endpoint by issuing the command:
`jspm registry create kendo jspm-git`
and use the following responses to the prompts you will get:

    - base URL: __https://bower.telerik.com__
    - Set advanced configurations? __yes__
    - Would you like to use the default git repository suffix (.git)? __yes__
    - Disable shallow git clones? __no__
    - Enable authentication? __yes__
    - Now enter your Telerik credentials
<br>
<br>

3. Run the following command to install the **PRO version of Kendo UI**:
`jspm install css jquery kendo-ui=kendo:bower-kendo-ui`
<br><br>

4. Open `config.js` and add one path mapping:  
  **Make sure that you reference the correct version of Kendo in the `kendo.*` map!**   
  
  ```
  paths: {
    "*": "dist/*",
    "github:*": "jspm_packages/github/*",
    "npm:*": "jspm_packages/npm/*",
    "kendo:*": "jspm_packages/kendo/*",
    "kendo.*": "jspm_packages/kendo/bower-kendo-ui@2016.2.714/js/kendo.*.js"    <----
  },
  "map": {
    "aurelia-bootstrapper": "npm:aurelia-bootstrapper@1.0.0-beta.1",
    "aurelia-fetch-client": "npm:aurelia-fetch-client@1.0.0-beta.1",
    "aurelia-framework": "npm:aurelia-framework@1.0.0-beta.1.0.2",
    "kendo-ui": "kendo:bower-kendo-ui@2016.1.226+SP1"
  }
  ```
  **Note:** old versions of Kendo require a jquery.min map that is the equivalent of the jquery map: "jquery.min": "github:components/jquery@2.1.4" 
<br><br>
5. Now let's open up "app.html" and load KendoUI's CSS files

    ```
    <require from="kendo-ui/styles/kendo.common.min.css!"></require>
    <require from="kendo-ui/styles/kendo.bootstrap.min.css!"></require>
    ```
<br><br>
***
***