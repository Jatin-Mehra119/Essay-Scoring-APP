# Essay Scorer Pro - Streamlit App

## Overview

**Essay Scorer Pro** is a Streamlit-based web application that uses AI to score essays on a scale of 1 to 6. Users can input essay text directly or upload a CSV file containing essays to get predictions. The model used for scoring is based on a pre-trained model from Hugging Face.

This app is deployed on **Hugging Face Spaces**, so it can be accessed directly from the web without needing to build or run Docker locally.

#### **Model Used**: [Smollm2-360M-Essay-Scoring](https://huggingface.co/jatinmehra/Smollm2-360M-Essay-Scoring)

#### **Development Repository**: [Essay-Scoring-Modeling](https://github.com/Jatin-Mehra119/Essay-Scoring-Modeling)
## Features

-   **Text Input**: Enter essay text to receive an AI-generated score.
-   **CSV Upload**: Upload a CSV file containing a column named `full_text` to score multiple essays at once.
-   **Model**: Uses a pre-trained Hugging Face model (`jatinmehra/Smollm2-360M-Essay-Scoring`) for scoring essays.

## How to Use

You can access the **Essay Scorer Pro** application directly by visiting the following Hugging Face Space URL:

-   [Essay Scorer Pro - Hugging Face Space](https://huggingface.co/spaces/jatinmehra/Essay-Scorer-Pro)

### Input Methods:

1.  **Enter Text**: Paste your essay text directly into the text input area and click on "Predict Score" to receive the AI-generated score.
2.  **Upload CSV File**: Upload a CSV file with a column named `full_text` containing the essays you want to score. After uploading, the app will generate scores for each essay in the file, and you can download the file with the predicted scores.

## Model and Cache

The Hugging Face model (`jatinmehra/Smollm2-360M-Essay-Scoring`) is automatically downloaded when you use the app for the first time. The model and other related files are cached in a directory within the app, which Hugging Face Spaces manages automatically.

## Troubleshooting

-   **Permission Errors**: If you encounter any issues with the app or model download, it's likely related to Hugging Face's infrastructure, and you can contact their support for help.
    
-   **Model Loading Issues**: If the model fails to load, ensure that the `full_text` column exists in your CSV file when uploading. The model needs properly formatted input to work correctly.
    

## Requirements

Since the app is hosted on Hugging Face Spaces, you do not need to manually install any dependencies. The Hugging Face platform takes care of the environment setup for you. However, here are the dependencies used in the app:

-   **streamlit**: For the web interface.
-   **pandas**: For handling CSV files.
-   **transformers**: For using Hugging Face models.
-   **torch**: For running PyTorch-based models.
-   **text-unidecode**: For text preprocessing.

## Contributing

Feel free to fork the repository or create an issue if you encounter any problems or have suggestions for improvements.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

----------

### Notes:

-   **Hugging Face Spaces**: You do not need to build or deploy the app manually. Simply use the provided Hugging Face Space URL to access the app.
-   **Model and Cache**: The Hugging Face platform handles the model caching and storage automatically. If you're using the app frequently, the model will be cached and loaded faster.