# facial-mood-music-recommender-AI
<!DOCTYPE html>
<html lang="en">

<body>

    <p> An emotion recognition model using Convolutional Neural Networks (CNNs) to classify facial emotions from images and then recommend a song based on the facial expression. The model is trained on a dataset containing images labeled with seven emotion categories: anger, disgust, fear, happiness, neutrality, sadness, and surprise. </p>

    <h2>Project Structure</h2>
        # This file
    </pre>

    <h2>Dependencies</h2>
    <ul>
        <li>opencv-python</li>
        <li>numpy</li>
        <li>matplotlib</li>
        <li>seaborn</li>
        <li>tensorflow</li>
        <li>scikit-image</li>
    </ul>

    <p>Install the required dependencies with:</p>
    <pre><code>pip install -r requirements.txt</code></pre>

    <h2>Getting Started</h2>

    <h3>1. Prepare Dataset</h3>
    <p>Organize the dataset into two directories: <code>train/</code> for training images and <code>validation/</code> for validation images. Each subdirectory should contain images of a specific emotion category.</p>

    <h3>2. Model Architecture</h3>
    <p>The CNN model includes the following layers:</p>
    <ul>
        <li>Conv2D, MaxPooling2D, and Dropout layers</li>
        <li>BatchNormalization for improved training stability</li>
        <li>Dense layers for classification (7 classes for emotions)</li>
    </ul>

    <h3>3. Training</h3>
    <p>The model is trained using data augmentation techniques to improve generalization. Training uses the Adam optimizer with categorical cross-entropy loss, and accuracy is used as the evaluation metric.</p>

    <h3>4. Save/Load Model</h3>
    <p>To save the trained model:</p>
    <pre><code>model.save("emotion_recognition_model.h5")</code></pre>

    <p>To load a saved model:</p>
    <pre><code>from tensorflow.keras.models import load_model
model = load_model("emotion_recognition_model.h5")</code></pre>

    <h2>Evaluation</h2>
    <p>The model's performance is evaluated on the validation dataset, with accuracy reported after each epoch.</p>
</body>
</html>
