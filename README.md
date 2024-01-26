# RecognitionModel
# Problem Statement:

Our task involves creating a unified model capable of classifying images into four distinct categories: HappyMale, HappyFemale, SadMale, or SadFemale. Two datasets are available for this purpose: one containing happy and sad faces, and another featuring male and female faces.

# Datasets:

1. Happy-sad Dataset:
Format: h5 file
Approximately 600 images with labels denoting happiness (1) or sadness (0).
2. Male-female Dataset:
Over 58,000 images categorized into training and validation folders.
Labels: "0" for female, "1" for male.

#Challenges Encountered:

The significant difference in data size between the two datasets posed challenges in our initial approaches:

1. Separate Model Training:
- Initial consideration involved training two separate models for each dataset.
- Combining outputs led to potential issues like overfitting due to dataset size imbalances.
2. Pretraining on Male-female Dataset:
- Contemplated pretraining the model on the larger male-female dataset.
- Application to the happy-sad dataset proved less effective due to biased labeling, impacting performance.
3. Transfer Learning Approach:
- Finalized a transfer learning approach.
- Independently trained an emotion model on the happy-sad dataset.
- Utilized this emotion model as a pretrained model for the male-female dataset.

# Approach:

1. Independent Emotion Model:
- Trained a model specifically for the happy-sad dataset to capture emotional nuances.
2. Transfer Learning:
- Applied the pretrained emotion model to the male-female dataset.
- Leveraged transfer learning to address biases in the happy-sad dataset.
- Aiming for a unified model capable of effectively handling both emotional and gender classifications.

This approach seeks to combine the strength of emotion recognition while mitigating biases, ultimately contributing to the development of a more accurate and robust unified model.

# Code Dependencies
![OS](https://img.shields.io/badge/OS-Any-brightgreen)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?logo=keras&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23189392.svg?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-%23013243.svg?logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-%23150458.svg?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-%23189392.svg?logo=python&logoColor=white)
![Random](https://img.shields.io/badge/Random-%23FF6F00.svg?logo=python&logoColor=white)
![H5py](https://img.shields.io/badge/H5py-%23D00000.svg?logo=python&logoColor=white)
![EarlyStopping](https://img.shields.io/badge/EarlyStopping-%23150458.svg?logo=python&logoColor=white)
![ModelCheckpoint](https://img.shields.io/badge/ModelCheckpoint-%23150458.svg?logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-%23FF6F00.svg?logo=scikit-learn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-%23013243.svg?logo=opencv&logoColor=white)
