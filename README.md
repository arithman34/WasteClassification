# Waste Classification Model

## Overview
This project implements an image classification model to identify different types of waste for recycling using the TrashNet dataset. The model is trained using **ResNet18**, and various optimisations such as **pruning** and **quantisation** are explored to improve deployment efficiency.

## Dataset
The model is trained on the **TrashNet** dataset, https://www.kaggle.com/datasets/feyzazkefe/trashnet, which consists of images categorised into six classes:
- **Cardboard**
- **Glass**
- **Metal**
- **Paper**
- **Plastic**
- **Trash**

## Model Performance
The model achieves the following classification performance on the test set:

| Class      | Precision | Recall | F1-Score | Support |
|------------|------------|------------|------------|------------|
| **Cardboard** | 1.00  | 0.92  | 0.96  | 61  |
| **Glass**     | 0.95  | 0.92  | 0.93  | 76  |
| **Metal**     | 0.88  | 0.92  | 0.90  | 62  |
| **Paper**     | 0.91  | 0.93  | 0.92  | 90  |
| **Plastic**   | 0.90  | 0.90  | 0.90  | 73  |
| **Trash**     | 0.79  | 0.86  | 0.83  | 22  |

**Overall Accuracy: 92%**

## Model Optimisations
### 1. **Pruning**
- **Purpose**: Reduces the number of model parameters by removing less important connections, making the model smaller and faster.
- **Effect**: Reduces size while maintaining reasonable accuracy.

### 2. **Quantisation**
- **Purpose**: Converts model weights from 32-bit floating point to 8-bit integers, reducing storage and improving inference speed.
- **Effect**: Decreases size with a slight accuracy tradeoff.

### 3. **Pruning + Quantisation**
- **Purpose**: Applies both pruning and quantisation for maximum compression.
- **Effect**: Achieves the smallest model with some accuracy loss.

## Model Size & Accuracy Comparison
TBC

## Deployment Considerations
- The optimised model is designed to be deployed on **mobile and embedded devices**.
- The model is **compressed using tar.gz format** for efficient storage.

## Future Work
- Improve the model’s robustness using a different dataset providing a more diverse and accurate waste environment.
- Increase the number of images for all classes ensuring increased diversity.
- Deploy as a **real-time mobile application**.

## Contributors
- **Arif A. Othman** (Machine Learning Engineer)

## License
This project is open-source under the MIT License.
