# Handwritten Character Recognition Using a Custom Neural Network

## Introduction
Handwritten character recognition is a challenging problem in computer vision. This project aims to develop a program that can accurately predict handwritten letters, improving text recognition and automation processes.

## Methodology
### Data Preprocessing
- Adjusted the label range from [1-26] to [0-25] to align with zero-based indexing.

### Model Architecture
- **Input Layer**: Images were flattened into a one-dimensional vector.
- **Hidden Layers**:
  - First hidden layer: 128 neurons with ReLU activation.
  - Second hidden layer: 64 neurons with ReLU activation.
- **Output Layer**: 26 neurons (one for each letter) with a softmax activation function.

### Model Compilation
- **Optimizer**: Adam
- **Loss Function**: Sparse Categorical Crossentropy
- **Evaluation Metric**: Accuracy

### Training
- **Callbacks**:
  - Learning Rate Scheduler: Adjusts the learning rate dynamically.
  - Early Stopping: Halts training when validation performance stops improving.
- **Training Parameters**:
  - Epochs: 20
  - Batch Size: 16

## Results
- **Test Accuracy**: 0.8897
- **Test Loss**: 0.3627

## Discussion
During model evaluation, signs of overfitting were observed. The model performed well on the training data but struggled with generalization on the validation set.

### Challenges Faced
- The Artificial Neural Network (ANN) had difficulty detecting meaningful patterns in the data, leading to poor generalization.

### Lessons Learned
- The importance of data preprocessing, architecture selection, and regularization techniques to improve performance and reduce overfitting.

## Conclusion
The results improved when the number of epochs was decreased and the batch size was increased, helping to reduce overfitting and stabilize training.

### Potential Improvements
- Explore using a Convolutional Neural Network (CNN) instead of a simple ANN. CNNs are more effective for image-based tasks as they can automatically extract spatial features, leading to better recognition accuracy.
