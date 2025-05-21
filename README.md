# ImageProcessing_Project
🚗 Image preprocessing and feature extraction pipeline for car images. Includes brightness/contrast adjustment, denoising, edge detection, Harris corner detection, and HOG features using OpenCV and scikit-image.
#  Car Image Preprocessing and Feature Extraction

This project provides a complete pipeline for preprocessing car images and extracting features to support tasks like license plate detection or car classification. It uses OpenCV and scikit-image to apply various enhancement and feature extraction techniques.

---

## 📁 Dataset

**Source:** [Kaggle - Car Plate Detection Dataset](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection?select=images)  
The dataset contains images of vehicles, some of which show license plates clearly. The images are used as input for the image preprocessing pipeline in this project.

---

## 🛠 Features & Processing Steps

1. **Image Loading & Validation**
   - Checks file existence and format support (`.jpg`, `.png`, `.tif`, etc.).
   - Displays an error if the file is missing, corrupted, or has an unsupported extension.

2. **Brightness & Contrast Adjustment**
   - Adjusts image brightness and contrast with configurable parameters.

3. **Gaussian Blur**
   - Applies a Gaussian filter to smooth the image and reduce noise.

4. **Image Denoising**
   - Uses Non-Local Means Denoising (`cv2.fastNlMeansDenoisingColored`) to clean up the image without losing important details.

5. **Edge Detection**
   - Converts the image to grayscale and applies the Canny edge detector.

6. **Corner Feature Detection**
   - Uses the Harris Corner Detector to highlight important corners/features in the image.

7. **HOG (Histogram of Oriented Gradients) Feature Extraction**
   - Extracts HOG features suitable for machine learning models.
   - Saves the HOG visualization image and prints the feature vector length.

---

## 📂 Output Directory

All processed images are saved in the directory:
