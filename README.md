# YOLOv11-Based Multiclass Detection of PCB Surface Defects

PCB surface defect detection using **YOLOv11** and the **Ultralytics YOLO framework** for automated inspection.

## 📌 Project Overview

This project implements a computer vision-based approach for detecting defects on Printed Circuit Boards (PCBs). The project uses PCB images and annotated JSON data, converts the annotations into YOLO-compatible formats, prepares training datasets, and trains YOLO models for automated defect detection.

## 🎯 Objectives

* Detect PCB surface defects automatically.
* Convert annotated PCB data into YOLO-compatible format.
* Prepare training and validation datasets.
* Train YOLOv11 models for object detection.
* Perform multiclass PCB defect inference.
* Visualize detected defects using bounding boxes.

## 🛠️ Technologies Used

* Python
* Google Colab
* YOLOv11
* Ultralytics
* OpenCV
* NumPy
* Pandas
* Matplotlib
* PyYAML

## 📂 Dataset Preparation

The project performs the following dataset-processing steps:

1. Reads PCB images and JSON annotations.
2. Extracts polygon annotation coordinates.
3. Converts polygon annotations into YOLO bounding-box format.
4. Creates training and validation datasets.
5. Generates `data.yaml` configuration files.
6. Visualizes images with their corresponding labels.

The dataset itself is not included in this repository.

## 🔍 Defect Classes

The multiclass inference section of the project uses the following classes:

* Good
* Excess Solder
* Poor Solder
* Spike

## ⚙️ Methodology

### 1. Data Preparation

Annotated PCB images are processed from JSON format and converted into YOLO-compatible labels.

### 2. Dataset Configuration

YOLO `data.yaml` files are generated with training, validation, class names, and class counts.

### 3. Model Training

YOLOv11 models are trained using the Ultralytics framework.

Example training configuration:

* Model: YOLOv11n
* Image size: 640 × 640
* Epochs: 100

### 4. Data Augmentation

Augmented datasets are prepared to improve model training and detection performance.

### 5. Detection

The trained model is used to perform inference on PCB images and generate annotated output images.



## 📊 Results

| Metric | Result |
|---|---:|
| mAP@0.5 | 84.02% |
| mAP@0.5:0.95 | 62.88% |
| Precision | 83% |
| Recall | 79% |

> **Note:** Only verified values from the final YOLO training results should be reported here.

## 📓 Notebook

The complete implementation is available in:

`YOLOv11_PCB_Defect_Detection.ipynb`

The notebook contains dataset preparation, annotation conversion, YOLO training, visualization, and inference steps.

## 🚀 How to Run

1. Open the notebook in Google Colab.
2. Install the required Python packages.
3. Mount Google Drive.
4. Provide the dataset path.
5. Prepare the YOLO dataset.
6. Configure the `data.yaml` file.
7. Train the YOLO model.
8. Run inference on PCB images.
9. Visualize the detection results.

## 👩‍💻 Author

**Shrinavya Illur**

Electronics and Communication Engineering
KLE Technological University
