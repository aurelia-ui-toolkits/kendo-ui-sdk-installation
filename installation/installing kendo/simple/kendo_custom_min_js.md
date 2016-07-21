# kendo.custom.min.js
Telerik has a nice feature on their website where they allow you to select a set of controls and download a minified javascript that only conatins the controls you selected. This is recommended as this file is often smaller in size than kendo.all.min.js.

1. [Log in](https://www.telerik.com/account)
2. Hover over the Products and Subscription menu, then click Kendo UI Professional
![img](http://i.imgur.com/jIggSWt.png)
3. Click on the "Build your custom download" banner
![img](http://i.imgur.com/INIvWuC.png)
4. Select the controls that you use on your website
5. Scroll to the bottom of the page and decide whether you would like to use Telerik's CDN or if you want to download a javascript file

### CDN
1. Copy the script tags and add them to the `head` section of `index.html`
![img](http://i.imgur.com/EwnTgY7.png)
2. Add Kendo styles to your index.html
```
  <link rel="stylesheet" href="http://kendo.cdn.telerik.com/2016.2.714/styles/kendo.common.min.css">
  <link rel="stylesheet" href="http://kendo.cdn.telerik.com/2016.2.714/styles/kendo.bootstrap.min.css">
```


### Javascript file
1. Click on the "Download" button to download kendo.custom.min.js:
![img](http://i.imgur.com/c1QiJ4L.png)

2. Create a folder called `kendo-sdk` next to your `src` folder
 ![img](http://i.imgur.com/8UjLOHX.png)
 3. Add kendo.custom.min.js to the `kendo-sdk/js/` folder. Also, download the latest Kendo release from the Telerik website ([instructions](./kendo_all_min_js.md)) and extract the following files from the ZIP into the `kendo-sdk` folder:
   - js/jquery.min.js
   - the styles folder
 ![img](http://i.imgur.com/czORt01.png)
 7. Open index.html and add the following script tags
```
    <script src="kendo-sdk/js/jquery.min.js"></script>
    <script src="kendo-sdk/js/kendo.custom.min.js"></script>
```
and the following `link` tags:
```
  <link rel="stylesheet" href="kendo-sdk/styles/kendo.common.min.css">
  <link rel="stylesheet" href="kendo-sdk/styles/kendo.bootstrap.min.css">
```
