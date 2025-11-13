# YOLOv11 Traffic Sign Detection

This folder contains code to train and evaluate a YOLOv11 object detection model on the traffic sign dataset.

## Contents
- `YOLOv11_setup.ipynb`: Notebook to prepare dataset and train YOLOv11
- `data/`: Will contain YOLO formatted dataset (images + labels)
- `runs/`: YOLO training outputs (automatically created)

## Steps Overview
1. Install ultralytics (provides YOLOv8+; placeholder for YOLOv11 API)
2. Convert your existing classification dataset into object detection format (bounding boxes). If you only have class folders without bounding boxes, you must create or approximate bounding boxes.
3. Prepare a `data.yaml` config file.
4. Train the model.
5. Validate & run inference.

## NOTE
If your dataset does not have bounding box annotations, YOLO cannot be trained directly. You will need to:
- Obtain a version of the dataset with bounding boxes (e.g. GTSRB detection annotations) OR
- Generate pseudo boxes (center-cropped) as a temporary workaround.

This example notebook includes a pseudo-label generator for demonstration.
