# CustomAnimatedToggleButton

The `CustomAnimatedToggleButton` is a customizable toggle button widget that provides smooth animation transitions between two states.

## Features

- Smooth animation transitions
- Customizable colors, sizes, and animations
- Supports onTap callbacks

## Installation

Add `P448_TSS_C2_S1_T-animated-toggle-buttons` folder on your respective app.




## Usage
- `value`: The initial value of the button (true for ON, false for OFF).
- `isGradient`: Whether to use gradient colors for the button.
- `onResult`: A callback function that is called when the button is tapped. It returns the new value of the button (true for ON, false for OFF).
- `height`: The height of the button.
- `width`: The width of the button.
- `inActiveColor`: The color of the button when it is in the inactive state.
- `activeColor`: The color of the button when it is in the active state.
- `backgroundColor`: The background color of the button.
- `inActiveGradientColors`: The gradient colors of the button when it is in the inactive state.
- `activeGradientColors`: The gradient colors of the button when it is in the active state.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
CustomAnimatedToggleButton(
    inActiveColor: Colors.grey,
    activeColor: Colors.green,
    onResult: (value) {
            print('Button value: $value');
        },
    )
```
