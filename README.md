# Face Mask Detection Project

This project implements a deep learning model to detect whether a person is wearing a face mask correctly, incorrectly, or not wearing one at all. The model is trained on a combination of datasets from Kaggle and MaskedFace-Net.

## Datasets Used

1. [Kaggle Face Mask Dataset](https://www.kaggle.com/datasets/omkargurav/face-mask-dataset) - Contains images of people without masks
2. [MaskedFace-Net](https://github.com/cabani/MaskedFace-Net) - Contains images of people wearing masks correctly and incorrectly

## Project Structure

The project is implemented as a Google Colab notebook with the following main components:

1. Data Preparation
   - Dataset download and extraction
   - Image preprocessing and organization
   - Data augmentation using ImageDataGenerator

2. Model Architecture
   - Deep learning model trained for three-class classification
   - Optimized for face mask detection (correct wear, incorrect wear, no mask)
   - Model saved in HDF5 format (e.g. *model*.h5)

3. Training
   - GPU-accelerated training on Google Colab
   - Early stopping to prevent overfitting

## Performance

The model achieves excellent performance with:
- F1 Score: 0.9931 (weighted average)
- Accuracy: 99.31% on the test set
- Confusion Matrix:

  | Predicted →<br>Actual ↓ | Correctly Worn | Incorrectly Worn | No Mask |
  |------------------------|----------------|------------------|----------|
  | **Correctly Worn**     | 594            | 10               | 0        |
  | **Incorrect Wear**     | 0              | 605              | 0        |
  | **No Mask**            | 0              | 1                | 373      |

- Trained on GPU using TensorFlow/Keras

## Requirements

- Python 3.x
- TensorFlow 2.x
- Kaggle API
- scikit-learn
- numpy
- matplotlib
- OpenCV

## Usage

1. Open the notebook in Google Colab
2. Mount your Google Drive
3. Run the cells sequentially to:
   - Download and prepare the datasets
   - Train the model
   - Evaluate performance
   - Make predictions on new images

## Project Status

This project was completed as part of CS 4210 course in Spring 2025 at Cal Poly Pomona.

## License

The datasets used in this project have their own respective licenses:
- Kaggle Face Mask Dataset: [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)
- MaskedFace-Net: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
