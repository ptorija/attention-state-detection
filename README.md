# Attention State Detection
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14999552.svg)](https://doi.org/10.5281/zenodo.14999552)

This study reviews and extends a previous EEG-based neurofeedback system for classifying mental states between focused, unfocused, and drowsy, using machine learning techniques. EEG data from five participants, recorded during a simulated train control task, was processed through signal filtering, feature extraction with Short-Time Fourier Transform (STFT), and classification using Logistic Regression, Random Forest, Support Vector Machine (SVM), and k-Nearest Neighbors (k-NN). The results showed an average accuracy of 92.08\%, surpassing those reported in the original study (Açı et al., 2019), with k-NN achieving the highest F1-score (0.999133). Further EEG analysis revealed that focused state was primarily associated with lower-frequency brain activity, whereas unfocused and drowsy states showed an increase in higher-frequency components. Specifically, brain activity in the 10–12 Hz range was consistently higher in the drowsy state, while the unfocused state exhibited sporadic increases. These findings offer valuable insights that could guide the development of more advanced EEG-based classification models in the future.


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

## License
This project is licensed under the terms specified in the `LICENSE` file.

