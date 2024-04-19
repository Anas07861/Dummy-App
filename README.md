# CustomImage

The `CustomImage` widget displaying images in Flutter applications. It supports loading images from network URLs, local file paths, svgs and assets. Additionally, it provides options for specifying placeholder images, applying a shimmer effect while loading, and more.

## Features
- Load images from network URLs, local file paths, or assets.
- Customize image fit, height, width, and border radius.
- Display placeholder images while loading.
- Apply shimmer effect during image loading.
- Support for SVG images.

## Installation
To use the CustomImage widget in your Flutter project, follow these steps:
- Add `P426_ALJ_C15_S1_T-custom-image` folder on your respective app.
- Add `ShimmerWidget` widget file from this path ".../lib/core/widgets/generic_widgets/shimmer_widget.dart".
- Add the following dependency to your `pubspec.yaml` file:
<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
  dependencies:
    cached_network_image: ^3.3.1
    flutter_svg: ^2.0.10+1
    figma_squircle: ^0.5.3
    flutter_cache_manager: ^3.3.1
```
- 


## Usage
To use the `CustomImage` widget, simply provide the required parameters:
- `imagePath`: The path to the image to be displayed.
- `lowResImagePath`: The path to a low-resolution version of the image for faster loading.
- `fit`: How the image should be fitted into the available space.
- `height`: The height of the image.
- `width`: The width of the image.
- `backgroundColor`: The background color of the image container.
- `borderRadius`: The border radius of the image container.
- `matchTextDirection`: Whether to match the text direction of the application.
- `isIcon`: Whether the image is an icon.
- `paddingValue`: Padding around the image.
- `cachedKey`: A key to cache the image.
- `appLogoImage`: The path to the app logo image to be displayed as a placeholder.
- `cacheManager`: A cache manager for caching the image.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
CustomImage(
  imagePath: 'https://example.com/image.jpg',
  lowResImagePath: 'https://example.com/low_res_image.jpg',
  fit: BoxFit.cover,
  height: 200,
  width: 200,
  backgroundColor: Colors.grey,
  borderRadius: SmoothBorderRadius.all(radius: 8),
  appLogoImage: 'assets/logo.png',
)
```
