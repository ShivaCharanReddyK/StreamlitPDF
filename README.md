# Ask Questions for PDF Application

This application is written in Python and uses the `streamlit`, `langchain`, `langchain_community`, `python-dotenv`, and `tempfile` libraries. It is designed to allow users to upload documents (PDF, DOCX, TXT) and ask questions about the content of these documents. The application uses a language model to generate responses to the user's questions.

## Prerequisites

Before running this application, you need to have Python installed on your system. You also need to install the following Python libraries:

- torch
- accelerate
- sentence_transformers
- streamlit_chat
- streamlit~=1.31.1
- faiss-cpu
- tiktoken
- huggingface-hub
- pypdf
- replicate
- docx2txt
- langchain

You can install these libraries using pip:

```bash
pip install streamlit langchain langchain_community python-dotenv tempfile
```

OR (to install libraries at a time)

Just Clone or download the Repo 

and use 
```bash
pip install -r requirements.txt
```

## How to Run the Application

To run the application, navigate to the directory containing the `app.py` file in your terminal and type:

```bash
streamlit run app.py
```

This will start the Streamlit server and open the application in your default web browser.

## How to Use the Application

Once the Streamlit application is running:

1. In the sidebar of the application, there's an option to upload documents. You can upload PDF files.
2. After uploading a document, you can ask questions about its content in the text input field labeled "Question:". After submitting a question, the application will generate a response.
3. The application maintains a chat history, displaying both the user's questions and the generated responses.

The application uses the `langchain` and `langchain_community` libraries to generate responses to the user's questions based on the content of the uploaded documents. The vector representations of the documents are generated using the `HuggingFaceEmbeddings` class from the `langchain_community.embeddings` module. The `FAISS` class from the `langchain_community.vectorstores` module is used to create a vector store from the documents. The `ConversationalRetrievalChain` class from the `langchain.chains` module is used to create a conversational chain that generates responses to the user's questions.
