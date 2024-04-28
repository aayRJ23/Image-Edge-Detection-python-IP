# Edge Detection using Fuzzy Logic

This Python script performs edge detection on an input image using fuzzy logic techniques. It applies the Sobel operator for gradient calculation and fuzzy logic thresholding to detect edges effectively.

## Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- NumPy

## Usage (Google Colab)

1. Open Google Colab and create a new notebook.
2. Copy and paste the code into each modular cells.
3. Upload your input image (img.jpg) to the same directory as the notebook.
4. Run the code cells to execute the edge detection script.
5. The original image and the edge-detected image will be displayed below the code cell.


## Explanation

The `EdgeDetection-IP.ipynb` script consists of the following main components:

- **Edge Detection Function**: This function performs edge detection using fuzzy logic techniques. It first converts the input image to grayscale using OpenCV's `cvtColor` function. Then, it applies the Sobel operator in both the x and y directions using `cv2.Sobel` to compute the gradient magnitude. Next, the gradient magnitude is thresholded using fuzzy logic. This is achieved by calculating the maximum and minimum gradient magnitudes and computing a threshold value as the average of these two values. The fuzzy thresholding operation is applied using NumPy's vectorized operations and the hyperbolic tangent function (`np.tanh`). Finally, the resulting fuzzy thresholded image is converted to an 8-bit unsigned integer format using NumPy's `astype` function.

- **Main Function**: The main function reads the input image using OpenCV's `imread` function. If the image is successfully loaded, it calls the edge detection function described above. The original input image and the edge-detected image are then displayed using the `cv2_imshow` function from the `google.colab.patches` module. If the input image cannot be read, an error message is displayed.



