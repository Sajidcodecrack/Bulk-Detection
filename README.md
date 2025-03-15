# Urban Lake Bulk Waste Classification

## Introduction
Urban lakes in Dhaka city are severely polluted with waste, impacting both the environment and aquatic ecosystems. This project aims to classify lake waste into **Bulk Waste** and **No Bulk Waste** using a deep learning approach based on the YOLOv8 model.

## Objective
The goal of this project is to develop a reliable classification model that can distinguish between bulk waste and non-bulk waste, aiding in waste management and cleanup efforts.

## Waste Categories
The model classifies lake waste into two categories:
- **Bulk Waste**
- **No Bulk Waste**

## Dataset Preparation
We collected and annotated **112 images** of lake waste, ensuring variation in lighting conditions, angles, and environmental factors. The dataset was manually labeled and preprocessed before training.

### Data Augmentation
To enhance model performance, we applied various data augmentation techniques, including:
- **Rotation**
- **Flipping**
- **Brightness adjustment**
- **Gaussian noise addition**

## Model Architecture
We used **YOLOv8** as the object detection and classification model due to its efficiency in real-time detection. The model was fine-tuned using our customized dataset.

### Training Parameters
- **Batch Size**: 16
- **Epochs**: 50
- **Optimizer**: Adam
- **Learning Rate**: 0.001
- **Loss Function**: Cross-Entropy Loss

## Evaluation Metrics
The model was evaluated using multiple performance metrics:

### Classification Performance
The confusion matrix and performance metrics were analyzed to assess the model’s effectiveness.

### Precision, Recall, and mAP Scores
| Class | Images | Instances | Precision | Recall | mAP50 | mAP50-95 |
|-------|--------|-----------|-----------|--------|-------|----------|
| All   | 112    | 112       | 0.997     | 1.000  | 0.995 | 0.994    |
| Bulk Waste | 61 | 61 | 1.000 | 1.000 | 0.995 | 0.995 |
| No Bulk Waste | 51 | 51 | 0.995 | 1.000 | 0.995 | 0.993 |

## Challenges Faced
- **Limited Dataset**: A small dataset made it difficult to achieve better generalization.
- **Environmental Variability**: Factors such as lighting and water reflections affected detection quality.

## Future Improvements
To improve classification performance, we plan to:
- **Expand the dataset** by collecting more images from various urban lakes.
- **Enhance augmentation techniques** to improve model robustness.
- **Experiment with other architectures** such as EfficientDet or Swin Transformer.
- **Deploy the model** in a real-world application for automated waste monitoring.

## Conclusion
This project represents a step toward automating waste classification in Dhaka’s urban lakes. While the model performs well, further refinements and dataset expansion will enhance its accuracy and usability in real-world applications.

---

### Repository Structure
```
Urban-lake-Bulk-Waste-Classification/
│── dataset/                # Annotated images and labels
│── models/                 # Trained YOLOv8 model weights
│── scripts/                # Training and evaluation scripts
│── results/                # Performance reports and metrics
│── README.md               # Project documentation
```

### Acknowledgments
We acknowledge the efforts of the team in data collection, annotation, and model training. Special thanks to contributors who supported this initiative.

