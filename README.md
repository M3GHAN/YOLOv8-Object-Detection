 # YOLOv8 Object Detection: Person and PPE Detection

This repository demonstrates object detection using the YOLOv8 model for detecting persons and personal protective equipment (PPE) such as hard hats, gloves, masks, and more. The project covers both the conversion of PascalVOC annotations to YOLO format and the implementation of the YOLOv8 model for object detection.

## Table of Contents
- [Overview](#overview)
- [Dataset Preparation](#dataset-preparation)
  - [Converting PascalVOC Annotations to YOLO Format](#converting-pascalvoc-annotations-to-yolo-format)
- [YOLOv8 Model Training](#yolov8-model-training)
- [Inference and Prediction](#inference-and-prediction)
- [Visualization](#visualization)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)

## Overview

This project aims to detect persons and various PPE items using a custom-trained YOLOv8 model. It includes:
- Converting XML annotations from the PascalVOC format to YOLO format.
- Training a YOLOv8 model on a custom dataset.
- Making predictions and visualizing the results with bounding boxes.

## Dataset Preparation

### Converting PascalVOC Annotations to YOLO Format

The dataset annotations provided in PascalVOC XML format need to be converted to YOLO format for training the YOLOv8 model. The conversion ensures that the annotations are in the required format for YOLO, where each line in the `.txt` file corresponds to an object in the image with normalized bounding box coordinates.

- The PascalVOC XML files should be stored in a directory (e.g., `/XML_Labels`).
- The converted YOLO annotations are saved in a separate directory (e.g., `/labels`).

## YOLOv8 Model Training

Once the dataset is prepared, the YOLOv8 model is trained using a custom dataset of images containing persons and PPE items. The dataset should include images and corresponding YOLO-format labels.

The model supports detection of the following classes:
- Person
- Hard-hat
- Gloves
- Mask
- Glasses
- Boots
- Vest
- PPE-suit
- Ear-protector
- Safety-harness

The training script handles loading images and annotations, training the model, and saving the best weights for later inference.

## Inference and Prediction

After training, the model can be used to make predictions on new images. The model outputs bounding boxes around detected objects, along with confidence scores and class labels.

The supported classes include:
1. Person
2. Hard-hat
3. Gloves
4. Mask
5. Glasses
6. Boots
7. Vest
8. PPE-suit
9. Ear-protector
10. Safety-harness

## Visualization

The project includes a visualization component that allows users to see the predictions overlaid on the input image. Bounding boxes are drawn around detected objects with labels indicating the class and confidence score.

The visualized image shows:
- Bounding boxes around detected objects.
- Class labels and confidence scores for each detected object.

## Results

The project demonstrates the effectiveness of YOLOv8 for detecting persons and PPE items. Results include high-confidence detections for various safety equipment in real-world images.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install the YOLOv8 model framework:
   ```bash
   pip install ultralytics
   ```

## Usage

1. Prepare your dataset by converting annotations to YOLO format.
2. Train the YOLOv8 model on your dataset.
3. Use the trained model to perform inference and visualize the predictions.

### Example Commands
- Convert annotations: [Instruction]
- Train the model: [Instruction]
- Make predictions: [Instruction]

## Acknowledgments

This project uses the YOLOv8 framework for object detection. Special thanks to [Ultralytics](https://github.com/ultralytics/ultralytics) for providing this powerful tool for object detection tasks.
