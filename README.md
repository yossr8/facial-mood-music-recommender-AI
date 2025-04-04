# Facial Mood Detection To Music-Recommender Using CNNs

An emotion recognition model using Convolutional Neural Networks (CNNs) to classify facial emotions from images and recommend a song based on facial expression. The model is trained on a dataset containing images labeled with seven emotion categories: anger, disgust, fear, happiness, neutrality, sadness, and surprise.

## Dependencies

The project requires the following Python libraries:

- `opencv-python`
- `numpy`
- `matplotlib`
- `seaborn`
- `tensorflow`
- `scikit-image`

You can install the required dependencies with:
pip install -r requirements.txt

## Getting Started

### 1. Prepare Dataset

Organize the dataset into two directories: `train/` for training images and `validation/` for validation images. Each subdirectory should contain images of a specific emotion category.

### 2. Model Architecture

The CNN model includes the following layers:

- `Conv2D`, `MaxPooling2D`, and `Dropout` layers
- `BatchNormalization` for improved training stability
- `Dense` layers for classification (7 classes for emotions)

### 3. Training

The model is trained using data augmentation techniques to improve generalization. Training uses the Adam optimizer with categorical cross-entropy loss, and accuracy is used as the evaluation metric.

### 4. Save/Load Model

```python
model.save("emotion_recognition_model.h5")
```
To load a saved model:
```python
from tensorflow.keras.models import load_model
model = load_model("emotion_recognition_model.h5"
```
### Evaluation
The model's performance is evaluated on the validation dataset, with accuracy reported after each epoch.
