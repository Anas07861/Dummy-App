# MarqueeTextView

`MarqueeTextView` is useful for displaying simple single-line texts with customizable properties. The default InkWell wrapper provides the onTap functionality for easy integration with interactive elements.

## Features
- Displays a single-line text with optional onTap callback.
- Supports customization of text properties such as color, size, style, weight, and alignment.
- Provides a default InkWell wrapper for onTap functionality.

## Installation
To use the `MarqueeTextView` widget in your Flutter project, follow these steps:
- Add `P426_ALJ_C1_S1_T-marquee-text-view` folder on your respective app.
- Add `DesignCustomInkWell` widget file from this path ".../lib/core/widgets/generic_widgets/design_custom_inkwell.dart".

## Usage
To use the `MarqueeTextView` widget, simply provide the required parameters:
- `text`: The text to be displayed.
- `textColor`: The color of the text. Defaults to white.
- `textSize`: The size of the text. Defaults to 14.0.
- `textAlign`: The alignment of the text within the widget. Defaults to TextAlign.right.
- `textFontStyle`: The font style of the text. Defaults to FontStyle.normal.
- `textFontWeight`: The font weight of the text. Defaults to FontWeight.w400.
- `onTap`: The callback function to be invoked when the text is tapped. Defaults to null.
- `textStyle`: Custom text style to override default text properties.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
MarqueeTextView(
  text: 'Hello, World!',
  onTap: () {
    print('Text tapped!');
  },
  textColor: Colors.blue,
  textSize: 18.0,
  textAlign: TextAlign.center,
  textFontWeight: FontWeight.bold,
)
```
