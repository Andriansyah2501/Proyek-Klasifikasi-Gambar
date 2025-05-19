# Flower Classification Model Submission

## Overview
This submission contains a fine-tuned MobileNetV2 model for classifying flower images into 5 classes: daisy, dandelion, rose, sunflower, and tulip. The model is provided in three formats: TensorFlow.js (TFJS), TensorFlow Lite (TFLite), and SavedModel.

## Directory Structure
- `tfjs_model/`: Contains TFJS model (`model.json` and `group1-shard1of1.bin`).
- `tflite/`: Contains TFLite model (`model.tflite`) and labels (`label.txt`).
- `saved_model/`: Contains SavedModel (`saved_model.pb` and `variables/`).
- `notebook.ipynb`: Jupyter notebook with model training, conversion, and inference code.
- `requirements.txt`: Python dependencies.
- `README.md`: This file.

## Model Details
- **Base Model**: MobileNetV2 (fine-tuned).
- **Input Shape**: (224, 224, 3).
- **Classes**: daisy, dandelion, rose, sunflower, tulip.
- **TFLite Accuracy**: 95.96% (test set: 1584 images).
- **Keras Accuracy**: 95.83% (test set: 1584 images).
- **TFLite Model Size**: 7.45 MB (dynamic quantization).

## Usage
1. **TensorFlow.js**:
   - Load `tfjs_model/model.json` in a JavaScript environment.
   - Preprocess input images to (224, 224, 3) and normalize to [0, 1].
2. **TensorFlow Lite**:
   - Use `tflite/model.tflite` with `label.txt` for inference on mobile/embedded devices.
   - Input: (1, 224, 224, 3), normalized to [0, 1].
3. **SavedModel**:
   - Load `saved_model/` in TensorFlow for serving or further training.
   - Input: (None, 224, 224, 3), normalized to [0, 1].

## Inference (Optional)
The TFLite model (`tflite/model.tflite`) is used for inference on 5 random test images in `notebook.ipynb`. Results include:
- **Input**: Images resized to (224, 224, 3) and normalized to [0, 1].
- **Output**: Predicted class (daisy, dandelion, rose, sunflower, tulip) and confidence score.
- **Example Results**:
  - Image 1: Predicted = daisy (Prob: 0.98), True = daisy
  - Image 2: Predicted = rose (Prob: 0.92), True = rose
  - ...
See `notebook.ipynb` for the complete inference code and visualization.

## Requirements
See `requirements.txt` for Python dependencies.

## Notes
- The dataset (6925 images) may contain duplicates across train/val/test sets. Data leakage check recommended.
- Contact: [Your Name/Email] for questions.