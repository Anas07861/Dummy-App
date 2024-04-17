# Firebase Remote Config

[![pub package](https://img.shields.io/pub/v/firebase_remote_config.svg)](https://pub.dev/packages/firebase_remote_config)

Firebase Remote Config is a cloud service that lets you change the behavior and appearance of your app without requiring users to download an app update. When using Remote Config, you create in-app default values that control the behavior and appearance of your app. Then, you can later use the Firebase console or the Remote Config backend APIs to override in-app default values for all app users or for segments of your user base. Your app controls when updates are applied, and it can frequently check for updates and apply them with a negligible impact on performance

## Usage
- ### Setting Up Firebase Remote Config:
    - Start by adding the necessary dependencies to your Flutter project's pubspec.yaml file.
    - You'll need `firebase_core: ^2.30.0`, `get: ^4.6.6` and `firebase_remote_config 4.4.2` packages.
    - Next, initialize Firebase in your app's entry point using `dart Firebase.initializeApp()` just as you would for other Firebase services.
<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
// Import Libraries
import 'package:firebase_core/firebase_core.dart';
import 'package:firebase_remote_config/firebase_remote_config.dart';

void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp(); // Add this line
  runApp(MyApp());
}
```
- ### Configuring Remote Parameters:
Navigate to the [Firebase Console](https://console.firebase.google.com), select your project, and open the "Remote Config" tab. Create parameter keys for values you want to configure remotely, such as text strings, feature toggles, or numerical values. Assign default values to these parameters, which will be used when fetching values from the server.

- ### Fetching Remote Values:
Use the `FirebaseRemoteConfig instance` to fetch remote values. Typically, you'll call `fetch()` to retrieve the latest values from the server and then call `activateFetched()` to apply these values to your app. Remember to set a default cache expiration time to ensure your app remains responsive even if fetching fails.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
class AppRemoteConfig {
  // Defaults Values
  Map<String, dynamic> _getDefaults() async {
    return <String, dynamic>{
       RemoteConstantsKeys.baseUrl: 'http://...',
     };
  }

  // Set Remote Config Data
  String get getBaseUrl => _remoteConfig.getString(RemoteConstantsKeys.baseUrl);
}
```

- ### Using Remote Values in Your App:
Once you've fetched and activated remote values, you can access them using the `FirebaseRemoteConfig instance`. For instance, you might use remote values to adjust text labels, control the visibility of UI components, or change app behavior based on different conditions.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
// Create Instance
final remoteConfig = AppRemoteConfig.instance;

// Use Remote Config value
String baseUrl = AppRemoteConfig.instance.getBaseUrl;

```
- ### Localization with remote config:
  - Add respective language specific json files on this "assets/local" path.
  - Put your remote config key in this json file created as shown below:
<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
{
  "testing_key":"Value testing AR",
}
```
  - Then run these commands:
      - flutter pub global activate get_cli
      - get generate locales assets/locales
  - Use with following syntax:
```dart
Text(
  LocaleKeys.testing_key.tr,
)
```
