# Skin Cancer Detection: An Ensemble Strategy

## Overview

This project focuses on enhancing the detection of skin cancer using an ensemble of Convolutional Neural Networks (CNNs). By leveraging multiple CNN architectures such as ResNet, AlexNet, VGG, and DenseNet, the project aims to improve classification accuracy through an ensemble approach. Additionally, the project explores the impact of image segmentation techniques, particularly contour-based segmentation, on the model's performance.

## Key Features

- **Ensemble of CNN Models**: Combines the strengths of ResNet18, AlexNet, VGG16, and DenseNet121 to improve the robustness and accuracy of skin cancer detection.
- **Segmentation Techniques**: Utilizes contour-based image segmentation to assess the impact of background skin color on model performance.
- **Evaluation Metrics**: The ensemble model is evaluated using accuracy and the Area Under the Precision-Recall Curve (AUC), with results compared to individual models and ResNet152.
- **Data Source**: Uses the HAM10000 dataset, reclassified into benign and malignant categories, to train, validate, and test the models.

## Project Structure

- **`data`**: Contains the HAM10000 dataset, split into training, validation, and testing sets.
- **`models`**: Includes the trained CNN models (ResNet18, AlexNet, VGG16, DenseNet121, ResNet152).
- **`segmentation`**: Implements contour-based segmentation using the `cv2` library.
- **`ensemble`**: Combines the outputs of individual models based on their testing accuracies.
- **`evaluation`**: Scripts to evaluate model performance using accuracy and AUC of the Precision-Recall curve.

## Methodology

1. **Data Preprocessing**: The HAM10000 dataset is preprocessed and split into segmented and non-segmented versions. The segmentation is performed using contour-based techniques.
2. **Model Training**: Five CNN models (ResNet18, AlexNet, VGG16, DenseNet121, ResNet152) are trained with consistent parameters across 25 epochs.
3. **Ensemble Method**: An ensemble of four models (ResNet18, AlexNet, VGG16, DenseNet121) is created by weighting their predictions according to testing accuracy.
4. **Performance Evaluation**: The ensemble and individual models are evaluated using accuracy and AUC of the Precision-Recall curve.

## Results

- The ensemble model outperformed most individual models, with a slight edge over the non-segmented data.
- ResNet152 showed comparable performance to the ensemble, indicating its strong potential in skin cancer detection.

## Contributions

- **Ananya Kulshrestha**: Developed the training/testing pipeline and ensemble method, ran experiments without segmentation, and performed ResNet152 evaluations.
- **David Chaudhari**: Handled data preprocessing, implemented contour and U-Net segmentation, and ran experiments with segmented data.

## Conclusion

The project demonstrates the potential of ensemble strategies and segmentation techniques in improving skin cancer detection. While the ensemble method showed promising results, ResNet152 performed comparably well, suggesting further exploration in future work.

## Future Work

- Explore alternative segmentation methods for better lesion isolation.
- Experiment with different ensemble strategies and parameter tuning.
- Investigate the use of Generative Adversarial Networks (GANs) to address data imbalance.

## Acknowledgements

Special thanks to the 6.8301 course staff for their guidance and support throughout this project, with particular appreciation to Dr. Pickering for his critical feedback.

## References

The project references relevant works on CNN models, segmentation techniques, and evaluation metrics. For detailed citations, refer to the project paper.
