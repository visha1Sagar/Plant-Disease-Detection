# Plant Disease Detection

This ~~DL Lab~~ project uses **MobileNet** and **transfer learning** to detect plant diseases across 38 different classes. The dataset comes from Kaggle's *New Plant Diseases Dataset* and is organized into train, validation, and test sets.

### Project Overview

- **Model**: MobileNet with pre-trained ImageNet weights.
- **Architecture**:
  - Input layer (224x224 images).
  - MobileNet as the base (with frozen weights).
  - Global Average Pooling.
  - Dropout for regularization.
  - Output layer with 38 softmax neurons for classification.
- **Optimizer**: Adam.
- **Metrics**: Accuracy, Precision, Recall.

### Steps to Run

1. **Download Dataset**: Use Kaggle CLI to download `new-plant-diseases-dataset.zip`.
2. **Extract Data**: Unzip the dataset and structure it into train/valid folders.
3. **Training & Validation**:
   - Data generators handle rescaling and batching.
   - Trained for 10 epochs; includes validation metrics.
4. **Evaluation**:
   - Test set evaluation shows loss, accuracy, precision, and recall.
   - Accuracy on the test set: ~96.8%.

### Visualizations

- Shows accuracy/loss plots.
![image](https://github.com/user-attachments/assets/0b0ebcb3-4464-46f2-9d72-bafac761fb9a)

- Random samples with predicted vs. actual labels.
![image](https://github.com/user-attachments/assets/90b6fa10-31d4-4cc5-955c-a0e391c02092)


### Code Highlights

- **Training & Validation Data**: Loaded with `ImageDataGenerator`.
- **Testing**: Evaluated on unseen test data to check generalization.
- **Visualization Function**: Displays predictions on sample test images.
