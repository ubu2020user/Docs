# Firebase Init
### Initialize Firebase in Flutter Project on new device
```bash
npm install -g firebase-tools
``` 
```bash
dart pub global activate flutterfire_cli
flutterfire configure
``` 
```bash
flutter build web
firebase init
# public directory: build/web
# Single-Page app?: yes
# Setup automatic builds and deploys with GitHub?: no
# Overwrite index.html?: no
``` 

### Add Hash to Firebase Authorized Apps
+ Get Android SHA1 & SHA256
```bash
cd android
./gradlew signingReport
```   
> Project Settings > General > Your Apps > Android > Add Fingerprint
+ Add them in firebase console and settings & android Project
+ Run FlutterFire configure to download new google-services.json automatically
```bash
flutterfire configure
```

# Stateful Widget
+ Be careful to update with via *setState* **if** a *fetch* is in the same build function
  + It will fetch every build again. Maybe **build functions only in stateless?**
```dart
FutureBuilder(
        future: _evaluateOTP(context),
        builder: (context, snapshot) {
          if (snapshot.connectionState == ConnectionState.waiting) 
```

# Auto Define 
+ Auto define the type of a variable is done via braces
```dart
void snackbar(BuildContext context, String message,
    {String? actionText, Function? onPressed})
```
+ In this case it is equal to 
```dart
void snackbar(BuildContext context, String message,
    {String? actionText = null, Function? onPressed = null})
```