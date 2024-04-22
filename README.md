# ScanQRCodeScreen Module

`ScanQRCodeScreen` module provides a comprehensive solution for scanning QR codes, including automatic scanning, manual entry, and validation. Customize the appearance and behavior according to your requirements.

## Features
- Scans QR codes using the device's camera.
- Displays a live camera view with a QR scanner overlay.
- Allows manual entry of codes through a bottom sheet.
- Provides validation for the manually entered code.
- Supports submitting and canceling the entry.

## Installation
To use the `ScanQRCodeScreen` module in your Flutter project, follow these steps:
- Add `P448_TSS_M4_S1_T-qr-scanner` folder on your respective app.



# ScanQRCodeScreenController Class

## Features
- Controls the behavior of the ScanQRCodeScreen.
- Handles camera permissions, QR scanning, manual code entry, and cleanup.

## Usage
To use the `ScanQRCodeScreenController` class, simply provide the required parameters:
- `isPermissionMessageShown`: Indicates whether the camera permission message has been shown.
- `getCodeController`: Controller for the manual code entry text field.
- `result`: The result of the QR code scan.
- `qrController`: Manages the QR scanner view.
- `formKey`: Key for the manual entry form.
- `qrKey`: Key for the QR scanner view.
- `checkPermissions`: Checks camera permissions and displays permission message if needed.
- `enterManuallyCodeBottomSheet`: Shows the bottom sheet for manual code entry.
- `onScanResult`: Handles the result of QR code scanning.
- `onClose`: Cleans up resources when the screen is closed.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
final controller = Get.put(ScanQRCodeScreenController());
```

# EnterManuallyCodeBottomSheetWidget Widget

## Features
- Provides a bottom sheet for manually entering QR codes.
- Validates the entered code and allows submission or cancellation.

## Usage
To use the `EnterManuallyCodeBottomSheetWidget` widget, simply provide the required parameters:
`controller`: The controller for the QR code screen.
`hint`: Hint text for the manual code entry field.
`cursorColor`: The color of the text cursor.
`textColor`: The color of the entered text.
`hintColor`: The color of the hint text.
`onChanged`: Callback for when the text field's value changes.
`onSubmitTap`: Callback for when the submit button is tapped.
`onCancelTap`: Callback for when the cancel button is tapped.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
EnterManuallyCodeBottomSheetWidget(
  controller: controller,
  onSubmitTap: () {},
);
```
