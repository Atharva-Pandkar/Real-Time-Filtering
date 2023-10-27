
# Real-Time-Filtering

This Application is used to explore different filters that can be attached to an image.
We have explored Computer VIsion applications on the image by performing the calculations manually.

## Grayscale 
This effect is accomplished by using the following relation between the pixels of a grayscale image and the BGR channel:

Gray = 0.11*Pixel of Blue Channel + 0.59*Pixel of Green Channel + 0.3*Pixel of Red Channel

The values for RGB channels are selected after learning about the luminosity of Grayscale
![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/9bab7ea3-0486-478e-b638-5325a5b7b968)
***

## Gaussian Filter 
The 1x5 filter is applied horizontally and the 5x1 filter is applied vertically.

![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/d5d42f42-2c9d-4ec9-9b14-167d1bd64d64)
***
## Sobel Filter

The Gradient Magnitude Image is generated with the help of 3x3 SobelX and SobelY separable filters.
![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/d64e21c6-078d-482b-b0f6-4cf0243c6cd3)
***

## Blur & Quantize the images
![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/6aa0b838-1f98-4fb6-98c0-e6411e894a74)
***
## Cartoonization 
![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/ead59db0-8adb-43b2-b9b7-324ec769150a)
***
## Negative
Implemented by subtracting each pixel value from 255
![image](https://github.com/Atharva-Pandkar/Real-Time-Filtering/assets/62322017/2ca6f1cb-db5f-495b-9d0b-d3c16156207b)
***
