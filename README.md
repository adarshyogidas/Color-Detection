Color Detection in Images using OpenCV

Objective:
This project detects the name of the color when the user double-clicks on a specific point in an image. It uses the RGB values of the pixel clicked and compares it to a dataset of color names.

Implementation:

Libraries Used:

cv2 (OpenCV): For image processing.
pandas: For handling the CSV dataset containing color information.
Steps:

Loading the Image and Dataset:
The image is loaded using OpenCV and resized to a fixed size. The color dataset is read using Pandas.

Mouse Callback Function:
A function draw_function is set up to capture the x and y coordinates when the user double-clicks on the image. The RGB values of the clicked pixel are stored.

Color Matching:
The function get_color_name computes the distance between the clicked color's RGB values and the dataset values to find the closest matching color.

Display Color Information:
A rectangle is drawn with the detected color, and the corresponding color name and RGB values are displayed as text over the image.

Design Choices:

Using Euclidean-like distance to find the closest color ensures simplicity and efficient matching.
Double-clicking allows the user to get precise color information without multiple clicks.
Challenges Faced:

Handling Bright Colors:
For bright colors, white text wasn't clearly visible, so a condition was added to switch to black text if the sum of RGB values is high.
