\#\#\# \[Webpack\]\(http://webpack.github.io/\)





&lt;p align=center&gt;

  &lt;img src="https://cloud.githubusercontent.com/assets/2712405/15518423/cb5a2252-21ca-11e6-816c-f4bcbc11a505.png"&gt;&lt;/img&gt;

 &lt;br&gt;&lt;br&gt;

&lt;/p&gt;



1. Install the bridge: \`npm install aurelia-kendoui-bridge --save\`

2. Open \`webpack.config.js\` and add the following to the \`coreBundles\`

\`\`\`javascript

  kendo: \[

    'aurelia-kendoui-bridge'

  \]

\`\`\`

3. While still in \`webpack.config.js\`, add the following line to \`baseConfig\`'s entry property:

\`\`\`

  'aurelia-kendoui-bridge': \['aurelia-kendoui-bridge'\]

\`\`\`

4. Now you can load wrappers of the aurelia-kendoui-bridge via \`&lt;require&gt;\` and they will be added to the webpack bundle

\`\`\`html

  &lt;require from="aurelia-kendoui-bridge/grid/grid"&gt;&lt;/require&gt;

  &lt;require from="aurelia-kendoui-bridge/grid/col"&gt;&lt;/require&gt;

\`\`\`

5. open main.js and register the plugin:

\`\`\`

    export function configure\(aurelia\) {

      aurelia.use

        .standardConfiguration\(\)

        .developmentLogging\(\)

        .plugin\('aurelia-kendoui-bridge'\);



      aurelia.start\(\).then\(a =&gt; a.setRoot\(\)\);

    }

\`\`\`

