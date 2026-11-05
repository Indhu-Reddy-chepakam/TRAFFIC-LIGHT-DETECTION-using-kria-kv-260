# BOSCH Traffic Light Detection Using YOLOv3-Tiny

## 1. Project Overview

This project focuses on detecting traffic lights in road images using the YOLOv3-Tiny object detection model and the BOSCH Small Traffic Lights Dataset.

The system identifies traffic lights and classifies them into eight categories. The detection results are displayed with bounding boxes and confidence scores.

## 2. Objectives

- Detect traffic lights in road images.
- Classify traffic lights into eight categories.
- Test the YOLOv3-Tiny model using different input images.
- Observe and analyse the detection results.

## 3. Technologies Used

- YOLOv3-Tiny
- Darknet Framework
- Python
- OpenCV
- BOSCH Small Traffic Lights Dataset

## 4. Traffic Light Classes

The model supports eight classes:

1. RedLeft
2. Red
3. RedRight
4. GreenLeft
5. Green
6. GreenRight
7. Yellow
8. Off

## 5. Project Structure

```text
BOSCH-TRAFFIC-LIGHT-DETECTION/
│
├── backup/
│   └── yolov3-tiny-bosch_40000.weights
│
├── outputs/
│   └── Detection result images
│
├── yolov3-tiny-bosch.cfg
├── voc-bosch.data
├── voc-bosch.names
├── train.txt
├── test.txt
├── bosch_voc_to_yolo_converter.py
├── train_test_split.py
├── make_xml_list.py
└── README.md
```

## 6. Implementation

The existing YOLOv3-Tiny implementation was set up using the Darknet framework.

The project configuration and class names were prepared for the BOSCH traffic-light dataset. The model was executed on test images, and the resulting detections were collected for analysis.

## 7. Output Results

The following folder contains screenshots of the detection results obtained during testing:

`outputs/`

## 8. How to Run

1. Clone this repository.
2. Set up the Darknet framework.
3. Download and prepare the BOSCH Small Traffic Lights Dataset.
4. Place the dataset in the directory structure expected by the dataset lists.
5. Check the paths in `voc-bosch.data`, `train.txt`, and `test.txt`.
6. Place the model weights in the `backup/` directory.
7. Run the YOLOv3-Tiny detection command using your Darknet installation.

Example command:

```bash
./darknet detector test voc-bosch.data yolov3-tiny-bosch.cfg backup/yolov3-tiny-bosch_40000.weights path/to/test_image.jpg
```

## 9. Reference

Original implementation:

https://github.com/berktepebag/Traffic-light-detection-with-YOLOv3-BOSCH-traffic-light-dataset

This project uses the original implementation as its starting point. The repository includes the project setup, testing work, and detection output screenshots.

## 10. Dataset

BOSCH Small Traffic Lights Dataset:

https://hci.iwr.uni-heidelberg.de/node/6132
