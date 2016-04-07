Ionic App Base + Purchase Corodova Plugin
==========================================

I'm having a real hard time getting this to work. I'm currently stuck at getting the [corodova plugin](https://github.com/j3k0/cordova-plugin-purchase) providing access to the store API to work.

I created this minimal setup roughly by executing the following steps:

```bash
$ npm run -- ionic start app-root blank
$ cd app-root
$ npm install --save ionic
$ npm install --save corodova
$ npm install --save deploy-ios
```
It still seems to be en vouge to install packages like ionic and cordova globally, which makes it impossible to see in the project code base which versions of theses packages are used in the project.
To circumvent this I add these packages to the packages.json too and include corresponding items in the scripts section that will execute binaries with the versions installed for that project.

```bash
$ npm run -- ionic plugin add 'https://github.com/j3k0/cordova-plugin-purchase.git#b15e9eed3480e85d3c87fd3d1c4dca58d2d163f9'
$ npm run -- ionic run ios --device
```

I added a little controller/view to test for the presence of the store object, but it does not get defined ..
