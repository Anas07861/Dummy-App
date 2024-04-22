# BottomNavBarScreen Module

`BottomNavBarScreen` screen displays a bottom navigation bar using the PersistentTabView widget from the persistent_bottom_nav_bar package. 

## Features
- It consists of a Scaffold with the body set to the PersistentTabView widget, which dynamically builds screens based on the selected index.

## Installation
To use the `BottomNavBarScreen` module in your Flutter project, follow these steps:
- Add `P448_TSS_M2_S1_T-bottom-nav` folder on your respective app.
- Add the following dependency to your `pubspec.yaml` file:
<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
  dependencies:
    persistent_bottom_nav_bar_v2: ^4.2.8
```


# BottomNavBarController Class

## Features
- This controller manages the state of the bottom navigation bar, including the selection of items and building screens.

## Usage
To use the `BottomNavBarController` class, simply provide the required parameters:
- `persistentTabController`: Controller for the PersistentTabView.
- `bottomBarItems`: List of BottomNavBarModel containing items for the bottom navigation bar.
- `selectedBottomIndex`: Index of the selected item in the bottom navigation bar.
- `buildScreens`: Builds the screens for the bottom navigation bar.
- `updateSelectedBottomIndex`: Updates the selected bottom index.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
final controller = Get.put(BottomNavBarController());
```

# BottomNavBarBindings Class

## Features
- This class is responsible for dependency injection for the BottomNavBarController.


# bottomNavBarItem Widget

## Features
- This function returns a `PersistentBottomNavBarItem` widget for the bottom navigation bar.

## Usage
To use the `PersistentBottomNavBarItem` class, simply provide the required parameters:
- `imagePath`: Image path for the item icon.
- `title`: Title of the item.
- `isActice`: Whether the item is active or not.
- `activeColor`: Color for active items.
- `inActiveColor`: Color for inactive items.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
BottomNavBarModel(imagePath: imagePath, title: title)
```
