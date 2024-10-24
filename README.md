# Exact-inference using bayesian networks (variable elimination)

# **Medical Diagnosis for Disease Symptom Detection using Bayesian Networks**

### **Project Overview**
This project uses a Bayesian Network model for disease diagnosis based on patient symptoms. The aim is to predict the most probable disease based on a set of symptoms, utilizing a dataset of various diseases and their associated symptoms. The Bayesian Network is built by calculating conditional probability distributions (CPDs) between diseases and symptoms, and inference is performed to predict diseases from observed symptoms.

### **Dataset**
The dataset(archive.zip) contains records of patients' symptoms and their diagnosed diseases. The symptoms are categorized, and for each patient, some symptoms may be missing (NaN). The dataset is cleaned, and missing values are filled based on the most common (mode) symptoms for each disease.

- **Columns in Dataset**:
  - `Disease`: The diagnosed disease.
  - `Symptom_1`, `Symptom_2`, ..., `Symptom_N`: Symptoms associated with the disease.

### **Setup and Installation**

1. **Clone or Download the Repository:**
   Clone this repository to your local machine or download the `.zip` file.
   ```bash
   git clone <repo-url>

2. **Install Required Libraries:**
   - pandas
   - numpy
   - scikit-learn
   - pgmpy
     
3. **Download the Dataset**:

   You can download the dataset from Kaggle and place it in the same directory as the notebook.
   If you use Colab, you can directly upload the dataset to Google Drive.

4. **Code Overview**
   
   - DATA PREPROCESSING:
     
      The dataset is loaded and cleaned by removing columns with excessive missing values.
      Missing values in the symptom columns are filled using the mode of the symptoms for each disease.
     
   - DATA ENCODING:
     
      The diseases are label-encoded to convert them into numeric form.
     Symptom columns are transformed into binary features using one-hot encoding to facilitate usage in the Bayesian Network.

   - BAYESIAN NETWORK MODEL:

      A Bayesian Network is defined, where each symptom is considered as a dependent variable (child) of the disease node (parent).
      Conditional Probability Distributions (CPDs) are calculated for the disease and the symptoms.
     
   - INFERENCE:

     The model is validated to ensure all CPDs are correctly defined.
     Variable Elimination is used for inference to predict the disease given a set of observed symptoms.
     
   - MODEL TESTING:

     The dataset is split into training and test sets.
     The model is tested on the test set, and accuracy is calculated based on how many correct disease predictions are made.

## Usage

### Run the Notebook:

1. Open the Colab Notebook (`.ipynb file`).
2. Run the cells sequentially to:
   - Build the Bayesian Network model.
   - Perform inference based on the trained model.
   - Evaluate the model’s performance using the test dataset.
  
## Results

- The model predicts diseases with an accuracy of **55%** for now based on the test data.

## Future Improvements

- Incorporate additional non-NaN symptoms or features to improve model performance and eventually the accuracy.
- Explore other probabilistic graphical models or machine learning approaches for disease prediction.


