# Firebase Init
+ Get Android SHA1 & SHA256
    + cd android/
    + ./gradlew-signing
+ Add them in firebase console und settings & android Project
+ Run FlutterFire configure to download new google-services.json automatically
+ flutter clean

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