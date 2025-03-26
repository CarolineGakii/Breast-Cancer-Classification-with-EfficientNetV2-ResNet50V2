# Breast Cancer Classification: EfficientNetV2 vs. ResNet50V2

## Project Overview

This project compares two convolutional neural networks—**EfficientNetV2** and **ResNet50V2**—in classifying histopathological images of breast cancer using the **BreakHis** dataset. The objective is to evaluate their performance in distinguishing between benign and malignant breast cancer cells.

## Dataset

This project uses the **BreakHis dataset** for training and evaluation.
The dataset consists of histopathological images of benign and malignant breast cancer tumors.

📌 **Download the dataset from Kaggle:**  

[BreakHis Dataset on Kaggle]


The **BreakHis** dataset comprises histopathological images categorized into benign and malignant classes. Initially organized by tumor types and magnification levels (40X, 100X, 200X, 400X), the dataset was restructured into two main directories for this study:

- `BreakHis/train/Benign/`
- `BreakHis/train/Malignant/`

This reorganization facilitated efficient data loading using TensorFlow's `image_dataset_from_directory` function.

## Models Used

- **EfficientNetV2**: Known for its efficiency and performance in image classification tasks.
- **ResNet50V2**: Renowned for its deep architecture and accuracy in computer vision applications.

## Training Details

- **Batch Size**: 32
- **Image Size**: 224x224
- **Optimizer**: Adam
- **Loss Function**: Binary Cross-Entropy
- **Learning Rate**: 0.0001
- **Epochs**: 
  - EfficientNetV2: 10
  - ResNet50V2: 5
- **Hardware**: CPU-based training

## Performance Metrics

- **EfficientNetV2**:
  - Validation Accuracy: Fluctuated between 66% and 70% over 10 epochs.
  - Training Loss: Remained around 0.61 to 0.64, indicating limited learning without significant overfitting.

- **ResNet50V2**:
  - Training Accuracy: Achieved 91.5% in just 5 epochs.
  - Validation Loss: Decreased from 0.33 to 0.18, suggesting effective learning and better generalization.

## Key Observations

1. **Training Speed**: 
   - EfficientNetV2 completed 10 epochs in 1,612 seconds.
   - ResNet50V2 had longer per-epoch training times.

2. **Performance**: 
   - ResNet50V2 achieved higher validation accuracy in fewer epochs.
   - EfficientNetV2 was faster but exhibited fluctuating validation accuracy.

3. **Resource Efficiency**: 
   - EfficientNetV2 required fewer computational resources compared to ResNet50V2.

## Challenges Faced

- **Dataset Organization**: The original dataset's complex structure necessitated manual reorganization to streamline the training process.
- **Training on CPU**: The absence of GPU resources led to longer training times.
- **Model Convergence**: EfficientNetV2 showed inconsistent validation accuracy, whereas ResNet50V2 demonstrated steady improvement.

## Conclusion

While **ResNet50V2** excelled in accuracy, it required longer training times. **EfficientNetV2** offered faster training with slightly lower accuracy. The choice between the two models depends on the specific requirements of accuracy versus computational efficiency.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---



