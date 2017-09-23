# Simple \(script tag\)

**Simple** KendoUI installation describes the case where the KendoUI SDK \(or its subset\) is loaded via the script tag in the application's `index.html` file, as depicted on the following screenshot

<p align=center>
  <img src="https://user-images.githubusercontent.com/2712405/30776582-e31c3278-a076-11e7-887f-56f594a8a5f4.png"></img>
<br>
Image 1
</p>

Observe that the above example fits the case of a JSPM based application (the folder **`@progress/kendo-ui@2017.3.913`** is contained in the **`jspm_packages/npm`** folder - meaning that the Kendo UI library was loaded by using this command:

 ```
jspm install npm:@progress/kendo-ui

```

which results with this layout on the local file system

<p align=center>
  <img src="https://user-images.githubusercontent.com/2712405/30776688-e97d9984-a078-11e7-8860-134efcc229d8.png"></img>
 <br>
 Image 2
</p>