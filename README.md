# ColorCatalog

## Project Description

The goal of this project is to select colors with specific abbreviations from available color atlases (Munsell and Pantone) and use them to reproduce a particular image.

### Color Selection Algorithm

The main idea of the algorithm is as follows:

1. We choose a pixel from the image and extract its 3 components: RGB.

2. We convert the RGB values of the pixel into the HSV color model to extract only one value for representing the color - the hue.

3. With this hue value, we search for corresponding abbreviations in the atlas with the same hue.

4. After finding a match in the atlas, we take the RGB values of that color and compare them to the original RGB values of the image pixel.

5. The comparison is done by summing the absolute values of the differences between the RGB components.

6. After finding a close color or a lack of correspondence, we update the so-called histogram.

7. If a close color is found, we increase the counter for the corresponding position in the color atlas histogram.

8. Otherwise, when there is no color match, we increase the counter of the last position in the histogram, representing discrepancies.

### Welcome Screen
![theScreen.png](https://github.com/Lyudmil02/ColorCatalog/blob/main/Images/theScreen.png)

### Button for load image
![LoadImageButton.png](https://github.com/Lyudmil02/ColorCatalog/blob/main/Images/LoadImageButton.png)

### Through these buttons you can choose which color scheme to work with
![PantoneMunsellButtons.png](https://github.com/Lyudmil02/ColorCatalog/blob/main/Images/PantoneMunsellButtons.png)

### Test image with Munsell color scheme
![testImage.png](https://github.com/Lyudmil02/ColorCatalog/blob/main/Images/testImage.png)

### Test image with Pantone color scheme
![testImagePantone.png](https://github.com/Lyudmil02/ColorCatalog/blob/main/Images/testImagePantone.png)
