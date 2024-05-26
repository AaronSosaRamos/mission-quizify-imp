# Gemini Quizify

## Index

- [Overview](#overview)
- [Key Features](#key-features)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Step-by-Step Installation Guide](#step-by-step-installation-guide)
- [Usage](#usage)
- [Tasks](#tasks)
- [License](#license)
- [Contact](#contact)

## Overview

Gemini Quizify is a sophisticated backend system developed in Python, designed to automate the creation of multiple-choice quizzes from a batch of loaded PDFs. This robust platform leverages advanced document processing and machine learning techniques to generate high-quality quizzes efficiently.

### Key Features

- **Batch PDF Loading:** Load multiple PDF documents at once for batch processing.
- **Document Processing for Embeddings:** Extract meaningful content from PDFs and convert them into embeddings for further analysis.
- **Vector Store Implementation:** Utilize a vector store to manage and retrieve embeddings efficiently.
- **Chain Implementation:** Implement a chain with setup_and_retrieval, prompt, and self.llm to streamline the processing workflow.
- **Question Generation with Prompt Design:** Use carefully crafted prompts to generate multiple-choice questions from the processed documents.
- **Streamlit UI Integration:** Present the generated questions in an intuitive and interactive user interface built with Streamlit, powered by VertexAI's large language model.

## Installation

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.10 or higher
- streamlit
- chromadb
- langchain
- langchain-google-vertexai
- pypdf
- Google Cloud access for VertexAI

### Step-by-Step Installation Guide

Follow these steps to set up the project on your local machine.

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/AaronSosaRamos/mission-quizify-imp.git
    cd mission-quizify-imp
    ```

2. **Create the Virtual Environment:**

    ```bash
    virtualenv venv
    source venv/bin/activate
    ```

3. **Install Dependencies:**

    Ensure all dependencies are installed by running:

    ```bash
    pip install -r requirements.txt
    ```

4. **Start the Project:**

    Navigate to the task directory and run the Streamlit application:

    ```bash
    cd tasks
    cd task_10
    streamlit run task_10_solution.py
    ```

5. **Access the Streamlit UI:**

    Open your web browser and navigate to [http://localhost:8501/](http://localhost:8501/) to access the Streamlit interface.

You are now ready to use Gemini Quizify! Load your PDFs, generate quizzes, and enjoy the streamlined experience provided by this powerful tool.

## Usage

1. **Load PDFs:** Use the interface to load a batch of PDFs into the system.
2. **Generate Questions:** The system will process the documents, extract content, and generate multiple-choice questions.
3. **Review and Export:** Review the generated questions and export them as needed.

## Tasks

1. **Google Cloud Configuration with VertexAI API Enabling and SDK Authentication with IAM User:**
   - Enable VertexAI API on your Google Cloud project.
   - Create an IAM user with the necessary permissions.
   - Set up SDK authentication by downloading the JSON key file and setting the `GOOGLE_APPLICATION_CREDENTIALS` environment variable.

2. **Clone the Project and Set Up the Development Environment:**
   - Clone the repository:
     ```bash
     git clone https://github.com/AaronSosaRamos/mission-quizify-imp.git
     cd mission-quizify-imp
     ```
   - Create a virtual environment and activate it:
     ```bash
     virtualenv venv
     source venv/bin/activate
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - If you encounter issues with Visual Studio Build Tools 2022, ensure they are installed and properly configured.
   - Set the environment variable for Google Authentication:
     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service-account-file.json"
     ```

3. **DocumentProcessor Class Creation:**
   - Implement the `DocumentProcessor` class to manage multiple PDF files using `PyPDFLoader`.
   - Ensure the class can load, parse, and prepare documents for embedding extraction.

4. **EmbeddingClient with VertexAI:**
   - Instantiate the `EmbeddingClient` class with VertexAI.
   - Generate embeddings from provided texts using the VertexAI embedding service.

5. **ChromaCollectionCreator for Vector Store:**
   - Create the `ChromaCollectionCreator` class to enable a ChromaDB for a vector store.
   - Relate document text with its embeddings for efficient retrieval.

6. **Use Streamlit UI for Testing:**
   - Test the functionalities of tasks 3 to 5 using the Streamlit UI.
   - Ensure documents are processed, embeddings are generated, and stored correctly.

7. **QuizGenerator Using LCEL:**
   - Develop the `QuizGenerator` class using the Langchain Execution Library (LCEL).
   - Chain the results based on ChromaCollection setup, prompt design, and LLM model (VertexAI).

8. **QuizGenerator Update:**
   - Implement the question generation feature in `QuizGenerator`.
   - Validate the generated questions and their JSON format.

9. **QuizManager for Navigation:**
   - Create the `QuizManager` class for navigating between Streamlit pages of the generated questions.
   - Ensure a smooth user experience for reviewing and managing quizzes.

10. **Final Test with All Provided Classes:**
    - Conduct a comprehensive test involving all classes: `DocumentProcessor`, `EmbeddingClient`, `ChromaCollectionCreator`, `QuizGenerator`, and `QuizManager`.
    - Verify the end-to-end functionality of loading PDFs, generating embeddings, creating quizzes, and navigating through the questions in the Streamlit UI.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

If you have any questions or need further assistance, please contact the project maintainer:

Aaron Sosa Ramos
[GitHub Profile](https://github.com/AaronSosaRamos)
