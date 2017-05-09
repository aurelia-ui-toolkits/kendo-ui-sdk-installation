### Installing the bridge
1. `npm install aurelia-kendoui-bridge --save`
2. in `ClientApp/app/boot.ts` add `.plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'));` like so:
   ```
   aurelia.use.standardConfiguration()
     .plugin(PLATFORM.moduleName('aurelia-kendoui-bridge'));
   ```

4. That's it!

