# Chat with Multiple PDFs using Gemini AI

This project allows users to upload multiple PDF files and interactively ask questions about the content using a chatbot powered by Google's Gemini AI. The system processes the PDFs, creates vector embeddings, and enables users to query the content in a conversational manner.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [License](#license)
- [Contributing](#contributing)

## Overview

This project provides an interactive Streamlit web application where users can upload PDF documents, process them into text chunks, and query the content using natural language. The application utilizes Google's Gemini AI models for embedding and conversational AI to provide detailed answers based on the content of the uploaded PDFs.

## Features

- **PDF Text Extraction**: Extracts text from uploaded PDF files.
- **Text Chunking**: Splits extracted text into manageable chunks for processing.
- **Vector Embeddings**: Converts text chunks into vector embeddings using Google Generative AI Embeddings.
- **Conversational AI**: Answers user queries based on the content of the uploaded PDFs using a custom chatbot powered by Gemini AI.
- **Interactive Interface**: User-friendly interface built with Streamlit for uploading files and asking questions.

## Installation

### Prerequisites

- Python 3.7 or higher
- Git

### Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/pdf-chatbot.git
    cd pdf-chatbot
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:

    - Create a `.env` file in the root directory with the following content:

      ```
      GOOGLE_API_KEY=your_google_api_key
      ```

    - Replace `your_google_api_key` with your actual Google API key.

## Usage

To run the application:

```bash
streamlit run app.py
```

## How It Works:

- **Upload PDFs**: Use the sidebar to upload one or more PDF files.
- **Process Files**: Click on "Submit & Process" to extract and process the text from the PDFs.
- **Ask Questions**: Enter your question in the input box, and the system will provide a detailed answer based on the content of the uploaded PDFs.

## Project Structure

- `app.py`: Main application file that handles the Streamlit interface and core functionality.
- `requirements.txt`: Lists all the dependencies required to run the project.
- `.env`: Environment variables file (not included in the repository; must be created by the user).
- `faiss_index/`: Directory where the vector embeddings are stored (created after running the application).

## Dependencies

The project uses the following dependencies:

- `streamlit`: For building the interactive user interface.
- `PyPDF2`: For extracting text from PDF files.
- `langchain`: For handling text chunking and conversational AI.
- `google-generativeai`: For generating embeddings and handling AI-powered chat responses.
- `faiss-cpu`: For efficient similarity search using vector embeddings.
- `python-dotenv`: For managing environment variables.

For a full list of dependencies, please refer to the `requirements.txt` file.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.
