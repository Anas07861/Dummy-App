# ImageSlider

The `ImageSlider` widget is a customizable image slider component for displaying a list of images with optional pagination indicators.
## Features
- Displays a list of images in a slider.
- Supports automatic sliding with customizable delay time.
- Optional pagination indicators (dots) to show current slide position.
- Customizable active and inactive colors for pagination indicators.
- Supports callback for page change events.

## Installation

- Add `CustomImage` widget file from this path ".../lib/core/widgets/generic_widgets/custom_image.dart".
- Add `P448_TSS_C1_S1_T-image-sliders` folder on your respective app.

## Usage
To use the `ImageSlider` widget, simply provide the required parameters:
- `sliderItems`: List of image URLs to display in the slider.
- `showDotedIndicator`: Boolean flag to control visibility of pagination indicators.
- `onPageChangeListener`: Callback function that is called when the page changes.
- `initialPage`: Initial page index to display when the slider is first loaded.
- `delayTimeInSecond`: Time interval (in seconds) for automatic sliding.
- `activeDotedIndicatorColor`: Color of the active pagination indicator.
- `inActiveDotedIndicatorColor`: Color of the inactive pagination indicator.
- `animationTimeDurationInMiliSeconds`: Duration of slide animation in milliseconds.

<?code-excerpt "readme_excerpts.dart (Write)"?>
```dart
ImageSlider(
  sliderItems: [
    'https://example.com/image1.jpg',
    'https://example.com/image2.jpg',
    'https://example.com/image3.jpg',
  ],
  showDotedIndicator: true,
  onPageChangeListener: (int pageIndex) {
    print('Page changed: $pageIndex');
  },
  initialPage: 0,
  delayTimeInSecond: 5,
  activeDotedIndicatorColor: Colors.blue,
  inActiveDotedIndicatorColor: Colors.grey,
  animationTimeDurationInMiliSeconds: 750,
)
```
