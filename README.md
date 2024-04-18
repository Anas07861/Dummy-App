# DotIndicator

The `DotIndicator` widget is a simple indicator component for displaying pagination dots.
## Features
- Displays pagination dots to indicate the current active index.
- Supports customization of dot size, spacing, and colors.

## Installation
Add `dot_indicator` folder on your respective app.

## Usage
To use the `DotIndicator` widget, simply provide the required parameters:
- `itemCount`: Total number of dots.
- `activeIndex`: Index of the currently active dot.
- `activeColor`: Color of the active dot.
- `inactiveColor`: Color of the inactive dots.
- `dotSize`: Size of the dots.
- `spacing`: Spacing between dots.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
DotIndicator(
  itemCount: 5,
  activeIndex: 2,
  activeColor: Colors.blue,
  inactiveColor: Colors.grey,
  dotSize: 10.0,
  spacing: 16.0,
)
```
