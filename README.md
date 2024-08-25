# Know Your Fit

## Overview

In the rapidly evolving world of e-commerce, especially within the fashion industry, the issue of returns and customer dissatisfaction due to incorrect sizing remains a significant challenge. This project introduces a groundbreaking Size Estimator and Virtual Try-On system designed to tackle this problem. By leveraging state-of-the-art AI and machine learning techniques, the system empowers shoppers to make informed decisions about their clothing fit and style with ease.

## Size Estimator

### Process Flow

1. **User Input**: Users begin by providing their height and uploading a photo.
2. **OpenPose Integration**: The system processes the photo using OpenPose to pinpoint key body landmarks.
3. **Contour Analysis**: A contour-based model in OpenCV is then used to accurately extract the contours of the user's body.
4. **Pixel to Centimeter Conversion**: The extracted measurements in pixels are converted into centimeters.
5. **Extreme Points Calculation**: Horizontal and vertical lines are drawn on the contours to determine the extreme points for shoulders, bust, hips, and waist.
6. **Size Calculation**: The system calculates the user's size by comparing the extreme points with the company’s size chart and leveraging previous data.

## Virtual Try-On

### Execution

To use the Virtual Try-On feature, execute the 'RantOn_Final.py' script with the following command:

```bash
python RantOn_Final.py <Path_to_File> <Path_to_Customer_Image> <Path_to_Apparel_Image>
```

### Supporting Files

1. **Apparel.py**: Manages the preprocessing of the apparel image for the try-on.
2. **Customer.py**: Handles the preprocessing of the customer’s image.
3. **Join.py**: Combines the apparel image with the customer’s image to create a realistic virtual try-on experience.

### Functions

- **grabcut()**: Isolates the necessary portion of the customer’s image and the existing clothing cutout.
- **userPreprocess()**: Decomposes the clothing cutout into sections at the joints for detailed analysis and sizing.
- **catPreprocess()**: Processes the new apparel image, resizing it to match the original clothing sections.
- **userFit()**: Aligns the modified apparel sections onto the customer’s image, creating a realistic visual representation.

## Conclusion

This project effectively addresses common issues in online apparel shopping. The Size Estimator and Virtual Try-On system enhance sizing accuracy and offer customers a virtual fitting room experience. This reduces uncertainty and improves the overall shopping experience, paving the way for a more confident and enjoyable journey in online fashion retail.
