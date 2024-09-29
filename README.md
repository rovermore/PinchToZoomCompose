📸 Jetpack Compose Image Zoom Library

A Jetpack Compose library that provides a simple and intuitive way to zoom in and out on images. Easily add pinch-to-zoom and double-tap gestures to your images in your Jetpack Compose projects.

Features

🔍 Pinch-to-zoom: Use two fingers to zoom in and out.
✋ Pan gesture support: Move the image around when zoomed in.
🖱️ Double-tap to zoom: Quickly zoom in and out with a double-tap.
🚀 Jetpack Compose-based: Leverages the power of Jetpack Compose for smooth and native Android experience.
🎨 Highly customizable: Adjust the maximum and minimum zoom levels and configure the pan boundaries.
Installation

Add the following to your project's build.gradle:

gradle
Copiar código
repositories {
    mavenCentral()
}

dependencies {
    implementation("com.yourcompany:imagezoom:1.0.0")
}
Usage

Here's a quick example of how to use the library:

kotlin
Copiar código
import androidx.compose.foundation.Image
import androidx.compose.runtime.Composable
import com.yourcompany.imagezoom.ZoomableImage
import androidx.compose.ui.res.painterResource

@Composable
fun ZoomableImageExample() {
    ZoomableImage(
        painter = painterResource(id = R.drawable.sample_image),
        contentDescription = "Sample Image"
    )
}
Customization
The ZoomableImage composable provides various parameters to customize the behavior of the zoom:

kotlin
Copiar código
ZoomableImage(
    painter = painterResource(id = R.drawable.sample_image),
    contentDescription = "Sample Image",
    modifier = Modifier.fillMaxSize(),
    maxZoom = 4f, // Maximum zoom level
    minZoom = 1f, // Minimum zoom level
    onZoomChanged = { zoomLevel ->
        // Handle zoom level changes here
    }
)
Parameters
Parameter	Description
painter	The image resource to display (required).
contentDescription	Content description for the image, for accessibility purposes.
modifier	Modifier to apply to the image (optional).
maxZoom	Maximum zoom level (default: 4f).
minZoom	Minimum zoom level (default: 1f).
onZoomChanged	Lambda function that gets called whenever the zoom level changes (optional).
License

Copiar código
Apache License 2.0
This library is licensed under the Apache License 2.0. See the LICENSE file for details.

Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.

Acknowledgements

Special thanks to the Jetpack Compose team and the Android community for their support and inspiration.

Contact

For any questions or support, please reach out to your.email@company.com.
