# Edge Detection using Fuzzy Logic

This repository contains a Python script for performing edge detection on images using fuzzy logic techniques. It applies the Sobel operator for gradient calculation and fuzzy logic thresholding to detect edges effectively.

## About

Edge detection is a fundamental step in image processing and computer vision tasks. It is used to identify boundaries and transitions in images, which is essential for various applications such as object detection, image segmentation, and feature extraction.

Traditional edge detection methods, such as the Sobel operator, can be sensitive to noise and may produce false detections in certain scenarios. Fuzzy logic provides a flexible approach to handle uncertainty and imprecision in image processing tasks. By incorporating fuzzy logic into edge detection algorithms, we can improve the robustness and accuracy of edge detection results.

## Features

- **Sobel Operator**: The script utilizes the Sobel operator to compute gradients in the horizontal and vertical directions, which are essential for edge detection.
- **Fuzzy Logic Thresholding**: Fuzzy logic thresholding is applied to the gradient magnitude to detect edges based on the intensity variations in the image.
- **Python Implementation**: The script is implemented in Python, making it easy to understand, modify, and integrate into existing projects.
- **OpenCV and NumPy**: The script leverages the OpenCV and NumPy libraries for image processing and numerical computing tasks, providing efficient and optimized operations.

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



