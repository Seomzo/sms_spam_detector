# Spam SMS Classification and UI

This project implements a spam SMS classifier using a machine learning pipeline built with Python, scikit-learn, and Gradio. The classifier is trained on the classic SMS Spam Collection dataset and then deployed via a simple web-based interface for quick predictions.

## What It Does

- **Data Loading & Preprocessing:**  
  Reads SMS messages from [Resources/SMSSpamCollection.csv](Resources/SMSSpamCollection.csv), cleans the text, and splits the data into training and testing sets.

- **Modeling:**  
  Uses a scikit-learn Pipeline that combines a `TfidfVectorizer` (with English stop words removed) and a `LinearSVC` classifier for spam detection. The model is trained using the training set and evaluated on the test set.

- **User Interface:**  
  A Gradio-based UI (see [gradio_sms_text_classification.ipynb](gradio_sms_text_classification.ipynb)) allows users to input a text message and receive a spam/ham prediction in real time.

## How It Works

1. **Dataset Preparation:**  
   The SMS Spam Collection dataset is loaded from the CSV file provided in the Resources folder. The messages and their corresponding labels ("ham" or "spam") are used to create a Pandas DataFrame.

2. **Training the Model:**  
   A Pipeline is defined:
   - **TF-IDF Vectorization:** Transforms the text messages into numeric feature vectors, removing common English stop words.
   - **SVM Classifier:** A LinearSVC is used to classify the messages.
   The pipeline is fitted on the training set and evaluated to ensure high accuracy.

3. **User Interface with Gradio:**  
   A simple UI is built using Gradio. Users can quickly test the classifier by entering their own SMS text. The UI shows the prediction result, classifying the message as either "spam" or "ham".

## How to Run

1. **Requirements:**  
   - Python 3  
   - Required libraries: `pandas`, `scikit-learn`, `gradio`

2. **Steps:**  
   - Open [sms_text_classification_solution.ipynb](sms_text_classification_solution.ipynb) to train and evaluate the model.
   - Open [gradio_sms_text_classification.ipynb](gradio_sms_text_classification.ipynb) to launch the UI.  
     Run the notebook cells to start the Gradio interface, which will provide a local URL for testing.

## Author

by Omar Alsadoon
