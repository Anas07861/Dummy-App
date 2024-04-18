# LargeText

The `LargeText` widget is a convenient way to display large text with customizable styling.
## Features

- Display text.
- Customize text style.

## Installation

Add `P426_ALJ_C3_S1_T- large-text` folder on your respective app.

## Usage
To use the `LargeText` widget, simply provide the required parameters:
- `title`: The text to display.
- `textColor`: The color of the text. If not provided, it will inherit the text color from the theme.
- `fontSize`: The size of the font. If not provided, it will inherit the font size from the theme.
- `textAlign`: The alignment of the text. If not provided, it will default to TextAlign.start.
- `maxLines`: The maximum number of lines to display before truncating. If not provided, it will display all lines.
- `fontWeight`: The weight of the font. If not provided, it will inherit the font weight from the theme.
- `fontFamily`: The font family to use. If not provided, it will inherit the font family from the theme.
- `textStyle`: A custom text style to apply to the text.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
LargeText(
  title: 'Your Large Text Here',
  // Additional optional parameters for customization:
  textColor: Colors.black, // Color of the text
  fontSize: 24, // Size of the font
  textAlign: TextAlign.center, // Alignment of the text
  maxLines: 2, // Maximum number of lines before truncating
  fontWeight: FontWeight.bold, // Weight of the font
  fontFamily: 'Roboto', // Font family
  textStyle: TextStyle(/* Custom text style */), // Custom text style
)
```
