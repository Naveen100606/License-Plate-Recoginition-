# License Plate Recognition

This project is a computer vision system for detecting and recognizing license plates from vehicle images. It uses OpenCV for image preprocessing, edge detection, and contour analysis to identify the license plate region. The text from the license plate is then extracted using Tesseract OCR.

## How it Works

1.  *Image Preprocessing*: The input image is resized and converted to grayscale. A bilateral filter is applied to reduce noise while keeping edges sharp.
2.  *Edge Detection*: The Canny edge detection algorithm is used to find edges in the grayscale image.
3.  *Contour Analysis*: Contours are found in the edged image. The contours are sorted by area, and the one that most closely resembles a rectangle (i.e., has four vertices) is assumed to be the license plate.
4.  *License Plate Extraction*: A mask is created for the identified license plate contour, and this mask is used to extract the license plate region from the original image.
5.  *OCR*: The extracted license plate image is then passed to Tesseract OCR to recognize and extract the text.
6.  *Visualization*: The original image with the detected license plate contoured, and the cropped license plate are displayed.

## Dependencies

  * OpenCV
  * imutils
  * NumPy
  * Pytesseract

## Usage

1.  Make sure you have Tesseract-OCR installed and provide the path to the executable in the script.
2.  Provide the path to the input image in the cv2.imread() function.
3.  Run the Python script.

## Results

The output of the script will be the detected license plate number printed to the console.


programming_fever's License Plate Recognition

Detected license plate Number is: MH 20 EE 7598
