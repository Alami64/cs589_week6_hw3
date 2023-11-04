# ChatGPT PDF Assistant

## Overview
ChatGPT PDF Assistant is a Streamlit web application that leverages OpenAI's GPT models to answer questions about the contents of a PDF document. By uploading a PDF, users can interact with the document in a conversational manner, asking questions and receiving responses based on the text extracted from the PDF.

## Features
- **PDF Upload**: Users can upload PDF documents to the application.
- **GPT Model Selection**: Choose between different GPT models (gpt-3.5-turbo or gpt-4) for generating answers.
- **Temperature Setting**: Adjust the temperature to balance between creativity and accuracy in responses.
- **Interactive Chat**: Engage with the PDF content through a user-friendly chat interface.
- **Vector Search**: Utilize vector search to retrieve the most relevant passages from the PDF for answering questions.

## Implementation
The application consists of several components working in conjunction:
- `PyPDFLoader`: Load and preprocess the content from PDF files.
- `RecursiveCharacterTextSplitter`: Divide the PDF text into overlapping chunks suitable for processing.
- `OpenAIEmbeddings`: Create embeddings for each chunk of text to facilitate search.
- `DocArrayInMemorySearch`: Index chunks and enable vector similarity searches.
- `ChatOpenAI`: Interface with the selected GPT model to generate responses.
- `ConversationalRetrievalChain`: Combine passage retrieval with answer generation for a seamless conversational experience.

The user interface is designed and built using Streamlit, providing an accessible and interactive experience.

## Setup

### Prerequisites
- requirements.txt

### Installation
To set up the ChatGPT PDF Assistant, follow these steps:

1. Clone the repository:
```
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/Alami64/cs589_week6_hw3.git)
```
2. Navigate to the project directory:
```
cd cs589_week6_hw3
```
3. Install the required Python packages:
```
pip install -r requirements.txt
```
4. Set up your OpenAI API key as an environment variable:
```
put you api key in .env file with variable name OPENAI_API_KEY
```

##Running the Application

To run the web application locally, execute the following command:
```
streamlit run webapp.py
```
The web application should now be accessible at `http://localhost:8501`
