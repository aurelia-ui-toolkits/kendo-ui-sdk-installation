# kendo.all.min.js

Kendo.all.min.js is a bundle of all controls from the Kendo PRO suite. It is 2MB+ in size, which is why we recommend to create a custom bundle of just the controls that you need in your application. Read more about this [here](./kendo.custom.min.js).

You could grab kendo.all.min.js by downloading the latest release from the Telerik website, or you could use Telerik's CDN.

### Telerik CDN
Add the following tags to `<head>` section of index.html

```
  <link rel="stylesheet" href="http://kendo.cdn.telerik.com/2016.2.714/styles/kendo.common.min.css">
  <link rel="stylesheet" href="http://kendo.cdn.telerik.com/2016.2.714/styles/kendo.bootstrap.min.css">

  <script src="http://code.jquery.com/jquery-1.9.1.min.js"></script>
  <script src="http://kendo.cdn.telerik.com/2016.2.714/js/kendo.all.min.js"></script>
  ```



### Downloading from Telerik website
1. [Log in](https://www.telerik.com/account)
2. Hover over the Products and Subscription menu, then click Kendo UI Professional
![img](http://i.imgur.com/jIggSWt.png)
3. Click on the Download button
![img](http://i.imgur.com/O5nQ7g6.png)
4. Click on the "Latest public version" button
![img](http://i.imgur.com/HELaUm1.png)

 5. Create a folder called `kendo-sdk` next to your `src` folder
 ![img](http://i.imgur.com/8UjLOHX.png)
 6. Extract the following files from the ZIP into the `kendo-sdk` folder:
   - js/kendo.all.min.js
   - js/jquery.min.js
   - the styles folder
 ![img](http://i.imgur.com/Up4Gduf.png)
 7. Open index.html and add the following script tags
```
    <script src="kendo-sdk/js/jquery.min.js"></script>
    <script src="kendo-sdk/js/kendo.all.min.js"></script>
```
and the following `link` tags:
```
  <link rel="stylesheet" href="kendo-sdk/styles/kendo.common.min.css">
  <link rel="stylesheet" href="kendo-sdk/styles/kendo.bootstrap.min.css">
```