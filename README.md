# LinkText

The `LinkText` widget displays text with clickable links. It allows you to customize the text style, link style, and behavior when a link is tapped.

## Features

- Display text with clickable links.
- Customize text style and link style.
- Option to trim URL parameters.
- Callback function for handling link taps.

## Installation

Add `P426_ALJ_C2_S1_T-link-text` folder on your respective app.




## Usage
To use the `LinkText` widget, simply provide the required parameters:
- `linkText`: The text content with links.
- `onLinkTap`: Callback function called when a link is tapped.
- `textStyle`: TextStyle for the non-link text.
- `linkTextStyle`: TextStyle for the link text.
- `textAlign`: Alignment of the text.
- `shouldTrimParams`: Whether to trim URL parameters.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
LinkText(
  linkText: 'Click here to visit www.example.com',
  onLinkTap: (url) {
    // Handle link tap
  },
)
```
