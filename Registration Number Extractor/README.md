# 🚦 Traffic Monitoring Project: Vehicle Registration Number Extraction 🚦

This project focuses on detecting vehicle registration plates using **YOLOv8** and extracting the registration numbers using **EasyOCR**. The solution can work with any type of license plate, including **HSRP** (High-Security Registration Plates), and doesn't require a specific format for successful detection.

### Key Sections:
- **Project Structure**: Describes all files and images included in the folder.
- **How It Works**: Provides a brief explanation of the detection and OCR pipeline.
- **How to Run**: Offers instructions to run both the notebook and the Python script.
- **Issues & Limitations**: Notes that the model requires more training.

## Project Structure

The following files are included in this repository:

### 1. **number_plate_detector.pt**
   - Pre-trained **YOLOv8** model for detecting vehicle registration plates.

### 2. **Registration_Number_Extraction.ipynb**
   - A Jupyter notebook that demonstrates the entire pipeline from detection to OCR-based number extraction.
   - Run this notebook to see how the model detects and extracts registration numbers from provided images.

### 3. **registration_number_extraction.py**
   - A Python script that replicates the steps in the notebook for those who prefer to run the pipeline in a Python environment.
   - You can modify this script for deployment or integration into other applications.

### 4. **Images**
   These are sample images included after testing. Each image contains a visible registration number that has been detected, extracted and shown.
   - **download.png**, 
   - **download (1).png**, 
   - **download (2).png**, 
   - **download (3).png**

## How It Works

1. **Object Detection**: The **YOLOv8** model detects the location of vehicle registration plates in the input images.
2. **Text Extraction**: **EasyOCR** is then used to read and extract the text (registration number) from the detected plates.
3. **Visualization**: Bounding boxes and extracted text are superimposed on the original images for easy visualization.

## How to Run

### Jupyter Notebook

1. Clone the repository:
    ```bash
    git clone https://github.com/akshaysatyam2/Traffic-Monitoring.git
    cd 'Traffic-Monitoring/Registration Number Extractor'
    ```
 and open the `Registration_Number_Extraction.ipynb` notebook in Jupyter or Google Colab.


2. Ensure all necessary libraries are installed (installation instruction already available in code file):
   ```bash
   !pip install ultralytics easyocr opencv-python
   ```

