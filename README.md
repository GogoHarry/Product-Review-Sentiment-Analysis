# Product-Review-Sentiment-Analysis

<video src="https://private-user-images.githubusercontent.com/82883963/360984159-27ec60e6-b168-495e-9d42-66caa1401957.mp4?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjQ0Mjc4MzYsIm5iZiI6MTcyNDQyNzUzNiwicGF0aCI6Ii84Mjg4Mzk2My8zNjA5ODQxNTktMjdlYzYwZTYtYjE2OC00OTVlLTlkNDItNjZjYWExNDAxOTU3Lm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA4MjMlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwODIzVDE1Mzg1NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPThhZjcwM2JhODkxOGI0ZDRjZTBlMzQ4Mzk5Zjk0NDdhNzA0YTA2MGM3NGY1OWU5ODU3Y2Q0OTM3NGExODgyMDcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.T-twcRou8v68a1fmPbcanhMqy1j7xBSXLvjRvMKwnFU" controls="controls" style="max-width: 100%;">
</video>

This project aims to build an end-to-end sentiment analysis solution that can extract, preprocess, analyze, and visualize customer sentiment from textual reviews. This solution will provide valuable insights to our business stakeholders, empowering them to make data-driven decisions and enhance the overall customer experience.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Web Application](#web-application)
- [Contributing](#contributing)
- [License](#license)

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/GogoHarry/product-review-sentiment.git
    cd product-review-sentiment 
    ```
2. Create a virtual environment:
    ```bash
    python -m sentiment_analysis_venv
    ```
3. Activate the virtual environment:
    - On Windows:
        ```bash
        sentiment_analysis_venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```bash
        source sentiment_analysis_venv/bin/activate
        ```
4. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Train the model and save the preprocessor and model:

2. Run the Streamlit web application:
    ```bash
    streamlit run app.py
    ```
## Features
- Predict the sentiment behind a review based on the review text
- Preprocess data using the preprocessing function
- Web interface for user-friendly interaction.

## Model Training

1. Preprocess data using the preprocessing function and save it
2. Vectorize the preprocessed data using TF-IDF vectorization and save the vectorizer
3. Train the Support Vector Machine model and save the model.

## Evaluation
Evaluate the model using accuracy_score, f1_score, and precision_score
```python
from sklearn.metrics import accuracy_score, precision_score, f1_score, classification_report, confusion_matrix

# Evaluation metrics
accuracy = accuracy_score(y_test, svc_y_pred)
precision = precision_score(y_test, svc_y_pred, average='weighted')
f1 = f1_score(y_test, svc_y_pred, average='weighted')

print(f"Accuracy: {accuracy:.4f}")
print(f"Precision: {precision:.4f}")
print(f"F1-Score: {f1:.4f}")

# Classification report
print("\nClassification Report:")
print(classification_report(y_test, svc_y_pred))

# Compute the confusion matrix
cm = confusion_matrix(y_test, svc_y_pred)

# Plot the heatmap
plt.figure(figsize=(8, 6))
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues', cbar=False, 
            xticklabels=['Negative', 'Positive'], yticklabels=['Negative', 'Positive'])
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.title('Confusion Matrix Heatmap')
plt.show()
```

# Web Application
1. Run the Streamlit app
```bash
streamlit run app.py
```
2. The app will be accessible at http://localhost:8501. Provide input text and get the sentiment behind the text

# Contributing
1. Fork the repository.
2. Create a new branch:
```bash
git checkout -b feature-branch
```
3. Commit your changes:
```bash
git commit -m "Add feature"
```
4. Push to the branch:
```bash
git push origin feature-branch
```
5. Create a pull request.

# License
This project is licensed under the MIT License - See the [LICENSE](LICENSE) file for details.
