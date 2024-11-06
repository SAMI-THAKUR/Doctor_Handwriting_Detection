# Doctor Handwriting Detection

This repository provides a deep learning solution for detecting and classifying handwritten doctor prescriptions. The project is structured into two main parts:

1. **Image Data Preparation**: Reads and saves prescription images in a compressed `.npz` format, allowing efficient data storage and faster loading for training purposes.
  
2. **Model Architecture and Training**: Defines a deep learning model with convolutional neural network (CNN) layers for feature extraction, combined with recurrent neural network (RNN) layers for sequence learning, aimed at accurate classification of handwriting patterns. Early stopping is implemented to prevent overfitting based on validation accuracy.

## Key Components

### Data Preparation

- **Image Loading and Preprocessing**: Images of handwritten prescriptions are read, resized, and converted into a format suitable for model training.
- **Data Saving**: All images and their labels are saved into a single `.npz` file, which allows for faster loading and consistent data handling across training sessions.

## Data Augmentation

To improve the model's generalization and prevent overfitting, **data augmentation** techniques are applied to the training images before training.

- **Rotation**: Random rotation of the images to help the model learn rotation-invariant features.
- **Zoom**: Random zooming to make the model more robust to size variations.

### Model Architecture

- **Convolutional Neural Network (CNN) Layers**: The model starts with multiple CNN layers that capture spatial features from the prescription images, identifying key patterns in handwriting.
- **Recurrent Neural Network (RNN) Layers**: Following the CNN layers, SimpleRNN layers are used to capture sequential dependencies in the handwriting, aiding in understanding the flow of text.
- **Dropout and Dense Layers**: Dropout layers help prevent overfitting, while dense layers further refine the output for final classification.

  ![image](https://github.com/user-attachments/assets/42f42e94-4f22-4c52-8386-98a447aa4283)
