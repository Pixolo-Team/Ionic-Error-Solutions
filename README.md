# Ionic-Error-Solutions
A list of the errors we have faced in Ionic and how we can solve them. This is a public repo feel free to Contribute.


## Firebase IID version issue:
[https://github.com/arnesson/cordova-plugin-firebase/issues/1081#issuecomment-504535565](https://github.com/arnesson/cordova-plugin-firebase/issues/1081#issuecomment-504535565)


[https://github.com/arnesson/cordova-plugin-firebase/issues/1081#issuecomment-503135862](https://github.com/arnesson/cordova-plugin-firebase/issues/1081#issuecomment-503135862)


## a.dex more than 64K
[https://stackoverflow.com/questions/36785014/the-number-of-method-references-in-a-dex-file-cannot-exceed-64k-api-17](https://stackoverflow.com/questions/36785014/the-number-of-method-references-in-a-dex-file-cannot-exceed-64k-api-17)


platform/android/app/build.gradle
### Put this inside your defaultConfig:
**multiDexEnabled true**

## Ionic Build Errors

### Could not find plugin "proposal-numeric-separator"

Install the plugin with this command
```
npm i @babel/plugin-proposal-numeric-separator
```

Add  
``` 
"resolutions": { "@babel/preset-env": "^7.8.7" } 
``` 
to package.json

    
Add the below lines in available-plugins.js
```
var _pluginTransformNumericSeperator = _interopRequireDefault(require("@babel/plugin-proposal-numeric-separator")); 
``` 
And 

``` 
"proposal-numeric-separator": _pluginTransformNumericSeperator,  (In _default var) 
```

 (path of the js file is node_modules/@bables/preset-env/lib/available-plugins.js)





### Ionic Serve gives this error: 
Error: EBUSY: resource busy or locked, rename
#### Solution: 
``` 
$ npm clear cache 
```
OR
Delete extra config files from C:\Users\Admin\.ionic\




