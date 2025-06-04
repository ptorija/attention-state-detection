# Attention State Detection
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15012034.svg)](https://doi.org/10.5281/zenodo.15012034)

This study reviews and extends a previous EEG-based neurofeedback system for classifying mental states between focused, unfocused, and drowsy, using machine learning techniques. EEG data from five participants, recorded during a simulated train control task, was processed through signal filtering, feature extraction with Short-Time Fourier Transform (STFT), and classification using Logistic Regression, Random Forest, Support Vector Machine (SVM), and k-Nearest Neighbors (k-NN). The results showed an average accuracy of 91.72\%, surpassing those reported in the original study (Açı et al., 2019), with k-NN achieving the highest F1-score (0.998142). Further EEG analysis revealed that focused state was primarily associated with lower-frequency brain activity, whereas unfocused and drowsy states showed an increase in higher-frequency components. Specifically, brain activity in the 10–12 Hz range was consistently higher in the drowsy state, while the unfocused state exhibited sporadic increases. These findings offer valuable insights that could guide the development of more advanced EEG-based classification models in the future.

In addition to the traditional machine learning models, an EEGNet architecture was implemented to assess its performance on the same EEG-based attention dataset. EEGNet, a compact convolutional neural network tailored for EEG signal processing, achieved a test accuracy of 96.16\% using Adam optimizer with a learning rate of 1e-3 and employed regularization techniques such as dropout (5\%), early stopping, and learning rate reduction on plateau to prevent overfitting.

## Requirements
Ensure you have Python 3.10+ installed.

## Installation
1. Clone this repository or extract the provided archive.

2. Navigate to the project directory:
   ```sh
   cd attention-state-detection
   ```
3. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   venv\Scripts\activate  # On Linux use: source venv/bin/activate
   ```
4. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage
1. Download the dataset

   Obtain the “EEG Data for Mental Attention State Detection” from Kaggle:
   https://www.kaggle.com/datasets/inancigdem/eeg-data-for-mental-attention-state-detection

   Unzip or extract the downloaded files into a folder named data in the project root. The directory tree should look like:
   ```sh
   attention-state-detection
   ┣ EEG_Data
   ┃  ┣ eeg_record1.mat.mat
   ┃  ┣ eeg_record2.mat.mat
   ┃  ┣ ...
   ┣ .gitignore
   ┣ LICENSE
   ┣ main_AI.ipynb
   ┣ main_ML.ipynb
   ┣ README.md
   ┗ requirements.txt
   ```
2. Activate the virtual environment (if not already active)

3. Install dependencies (if not already installed)

4. Run the notebooks
   - main_ML.ipynb: Executes the machine learning pipeline (Logistic Regression, Random Forest, SVM, k-NN).

   - main_AI.ipynb: Executes the deep learning pipeline using the EEGNet architecture.

5. Each notebook will load the .mat files from the EEG_Data folder, preprocess the EEG signals, train the models, and display performance metrics (accuracy, F1-score, confusion matrices, etc.).

## License
This project is licensed under the terms specified in the `LICENSE` file.

