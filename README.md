# YOLO-based Vehicle Detection & Benchmarking

## Overview

This project implements a vehicle detection pipeline using YOLO models to detect and classify vehicles across 6 categories. YOLOv5s and YOLO26n are trained and benchmarked to compare detection accuracy and inference performance.

## Dataset

- 3,000 labeled vehicle images
- 2,100 training images
- 900 validation images
- 6 classes: Car, Three-wheeler, Bus, Truck, Motorbike, Van

## Models

- YOLOv5s
- YOLO26n

Both models were trained using the same dataset and training configuration for a fair comparison.

## Results

| Model | mAP@0.5 | mAP@0.5:0.95 | Inference |
|-------|----------|---------------|-----------|
| YOLOv5s | 97.06% | 87.08% | 28.13 ms/image |
| YOLO26n | 94.37% | 87.30% | 24.82 ms/image |

YOLO26n achieved **11.8% faster inference** than YOLOv5s while maintaining comparable detection accuracy.

## Pipeline

```text
Dataset
   ↓
Data Preparation
   ↓
YOLO Training
   ↓
Validation
   ↓
Performance Evaluation
   ↓
YOLOv5s vs YOLO26n Benchmarking
```

