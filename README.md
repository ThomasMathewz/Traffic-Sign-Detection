# Traffic Sign Classification using Deep Learning

## Overview
This project focuses on building and evaluating deep learning models to classify traffic signs into 43 categories. Both custom Convolutional Neural Networks (CNNs) and transfer learning models were implemented to compare performance and identify the most effective approach.

---

## Objectives
- Perform image preprocessing and data augmentation
- Train multiple deep learning models for multi-class classification
- Compare model performance using evaluation metrics
- Identify the best-performing model for deployment

---

## Dataset
The dataset consists of traffic sign images organized into:
- **Train**: Images grouped into 43 class folders (0–42)
- **Test**: Unlabeled images
- **Meta**: Sample/reference images



Dataset Link: https://d3ilbtxij3aepc.cloudfront.net/projects/AI-Capstone-Projects/PRAICP-1002-TrafSignDetc.zip



---

## Project Structure
```

PRAICP-1002-TrafSignDetc/
│
├── Train/
│   ├── 0/
│   ├── 1/
│   └── ...
│
├── Test/
├── Meta/
├── notebook.ipynb
└── README.md

```

---

## Data Preprocessing
- Removed non-image files
- Resized images to a uniform shape
- Applied normalization and model-specific preprocessing
- Performed data augmentation:
  - Rotation
  - Zoom
  - Shift
  - Brightness adjustment

---

## Models Implemented
### Custom CNN Models
- cnn1
- cnn2
- cnn3

### Transfer Learning Models
- vgg_model (VGG16)
- resnet_model (ResNet50)
- eff_model (EfficientNetB0)

---

## Model Performance

| Model         | Validation Accuracy |
|--------------|-------------------|
| vgg_model     | ~98.99% |
| cnn2          | ~91.26% |
| resnet_model  | ~83.29% |
| eff_model     | ~76.30% |
| cnn1          | ~56.96% |
| cnn3          | ~15.27% |

---

## Key Insights
- Transfer learning significantly improves performance
- VGG16 achieved the best results due to strong feature extraction
- Custom CNN (cnn2) performed competitively
- Model performance depends heavily on preprocessing and fine-tuning

---

## Evaluation Metrics
- Accuracy
- Loss
- Confusion Matrix
- Classification Report

---

## How to Run
1. Mount Google Drive in Colab
2. Upload dataset zip file
3. Run all cells in the notebook
4. Train models and compare results

---

## Requirements
- Python 3.x
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## Future Improvements
- Hyperparameter tuning
- Grad-CAM visualization
- Model optimization for deployment
- Integration with web applications (Django/Flask)

---

## Conclusion

In this project, multiple deep learning models were developed and evaluated for the task of traffic sign classification using a dataset consisting of 43 classes. The models included three custom convolutional neural networks (cnn1, cnn2, cnn3) and three transfer learning models (vgg_model, resnet_model, eff_model).

From the experimental results, it is evident that the VGG16-based model (vgg_model) achieved the highest validation accuracy of approximately 98.99% with the lowest validation loss, making it the most effective model among all those implemented. This superior performance can be attributed to the use of pretrained weights, which enable the model to leverage rich and generalized feature representations learned from large-scale datasets.

The custom CNN model (cnn2) also performed well, achieving over 91% validation accuracy. This indicates that a carefully designed convolutional architecture, even without pretrained weights, can learn meaningful features for traffic sign recognition. However, it still falls short compared to transfer learning approaches in terms of generalization.

The resnet_model and eff_model showed moderate performance, with accuracies of approximately 83% and 76% respectively. These results suggest that although these architectures are powerful, their performance is sensitive to factors such as input size, preprocessing, and fine-tuning strategy. With further optimization, these models could potentially achieve higher accuracy.

On the other hand, cnn1 and cnn3 performed poorly, indicating that shallow or less optimized architectures are insufficient for capturing the complexity of multi-class image classification tasks involving fine-grained visual differences.

Overall, the results demonstrate that transfer learning significantly enhances model performance in image classification tasks, especially when the dataset is limited in size or diversity. Among all models, vgg_model is selected as the final model due to its high accuracy, low loss, and stable learning behavior.

Future work can focus on improving model interpretability using techniques such as Grad-CAM, optimizing hyperparameters, and deploying the model in a real-time application using web frameworks such as Django or Flask.



