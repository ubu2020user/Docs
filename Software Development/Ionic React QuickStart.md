# Table of contents
- [Table of contents](#table-of-contents)
- [Package.json](#packagejson)
- [Index.tsx](#indextsx)
- [App.tsx to index.tsx](#apptsx-to-indextsx)
- [Capacitor](#capacitor)
    - [For livereload:](#for-livereload)


# Package.json
1. "start": "ionic serve"
2. "build": "ionic build"
3. Move testing and types libraries from dependencies to devDependencies
     1. Just flavour 😉
4. Terminal => rm package-lock.json
5. Terminal => Npm install
6. Npm install @ionic/cli --save-dev --save-exact

# Index.tsx
1. Import {Plugins} from '@capacitor/core';
2. After import .theme....
3. const {SplashScreen} = Plugins;
4. After ReactDOM.render
5. SplashScreen.hide()

# App.tsx to index.tsx
+ Move imports of @ionic and ./theme

# Capacitor
+ Be aware of your version number... (watch udemy..)

### For livereload:
1. Ionic build
2. Ionic capacitor add android
3. Ionic cap open android
    1. Opens AndroidStudio
4. => Run in emulator
5. Ionic capacitor run android –livereload –external