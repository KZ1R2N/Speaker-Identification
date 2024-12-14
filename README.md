# Speaker Identification Using Bangla Dataset

## 🔍 Overview
This project demonstrates a Speaker Identification system using a custom Bangla dataset. The dataset consists of voice recordings from 26 unique individuals speaking 20 different sentences. The goal was to classify the speakers based on their voice characteristics using deep learning techniques. The process includes audio feature extraction, synthetic data augmentation, and model training.

## 📊 Features
- **Custom Bangla Dataset**: Voice recordings of 26 speakers.
- **Audio Feature Extraction**: Converted audio to gammatonegram images.
- **Data Augmentation**: Applied Synthetic Minority Oversampling Technique (SMOTE) to balance the dataset.
- **Deep Learning Model**: Used ResNet50 for feature extraction and classification.
- **High Accuracy**: Achieved 99% accuracy in speaker identification.

## 📂 Dataset
The dataset consists of:
- **26 folders** named after the speaker labels.
- Each folder contains multiple audio recordings of the respective speaker.
- **20 unique sentences** spoken by each speaker.

### Preprocessing Steps
1. **Gammatonegram Conversion**:
   - Each audio recording was converted into a gammatonegram image to represent the audio features visually. 
   - A gammatonegram is a time-frequency representation inspired by human auditory perception, capturing critical sound details essential for speaker identification.

2. **Feature Extraction**:
   - Leveraged the ResNet50 pre-trained model to extract high-level features from the gammatonegram images.

3. **Data Augmentation**:
   - Synthetic data was generated using SMOTE to address the small dataset size and ensure balanced class representation.

## 🌐 Gammatonegram Images
Gammatonegram images are a visual representation of audio signals, particularly well-suited for capturing spectral and temporal characteristics. Below is an example of a gammatonegram generated during preprocessing:

![Gammatonegram Example](Images/GammatonegramExample.PNG)

- The horizontal axis represents time.
- The vertical axis represents frequency bands.
- The intensity of the colors shows the energy levels across different frequencies and times.

These images are crucial for extracting features that help in distinguishing between speakers.

## 🔧 Model Architecture
1. **Feature Extraction**:
   - Utilized ResNet50 to process gammatonegram images and extract meaningful features.

2. **SMOTE Application**:
   - Applied SMOTE on the extracted features to generate synthetic samples for minority classes.

3. **Classification**:
   - Used the augmented feature set to train the final classification model.

## 🎯 Results
The model achieved an impressive **99% accuracy** on the test set, demonstrating its effectiveness in speaker identification.


