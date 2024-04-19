# ImageBorderColor

`ImageBorderColor` widget is useful when you need to add a border around an image or any other widget in your app.

## Features
- Provides an option to add a border around a child widget.
- Supports customizing the border radius and border color.
- Allows toggling the visibility of the border.

## Installation
To use the ImageBorderColor widget in your Flutter project, follow these steps:
- Add `image_border` folder on your respective app.
- Add `dimentions` file from this path ".../lib/utils/constants/dimentions.dart".
- Add the following dependency to your `pubspec.yaml` file:
<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
  dependencies:
    figma_squircle: ^0.5.3
```
- 


## Usage
To use the `ImageBorderColor` widget, simply provide the required parameters:
- `borderRadius`: Border radius of the container (optional).
- `child`: The widget to which the border will be applied.
- `isBorderColorShow`: Whether to show the border around the child widget (default: false).

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
ImageBorderColor(
  borderRadius: SmoothBorderRadius.all(radius: 20),
  isBorderColorShow: true,
  child: Image.asset('assets/image.jpg'),
)
```
