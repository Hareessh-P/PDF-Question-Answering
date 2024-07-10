# PDF Question Answering Bot :robot: :page_facing_up:

## Introduction to the Project

This project aims to develop a bot capable of answering questions from multiple uploaded PDF documents. Users can upload PDFs, ask questions related to the content of these documents, and receive relevant answers from the bot.

## Objective :dart:

The primary objective is to create an interactive web application that facilitates easy querying of information from PDFs, enhancing document accessibility and searchability.

## Technologies Used :computer:

- **Streamlit**: Used for building the interactive web application.
- **PyPDF2**: Utilized for extracting text from PDF documents.
- **LangChain**: Integrated for text processing, embeddings, vector stores, and conversational models.
- **OpenAI GPT-3 Model**: Employed for generating responses to user queries.
- **FAISS**: Implemented for efficient similarity search over document embeddings.

## Workflow :clipboard:

1. **PDF Text Extraction**: PDF documents are uploaded and processed using PyPDF2 to extract text content.

2. **Text Chunking**: Text from PDFs is segmented into manageable chunks using LangChain's CharacterTextSplitter.

3. **Vectorization**: The segmented text is converted into embeddings using OpenAI's embeddings or Hugging Face models via LangChain.

4. **Conversation Chain**: LangChain's ConversationalRetrievalChain is set up to handle user queries based on the vector store, providing relevant responses.

## User Interaction :speech_balloon:

- **Interface**: The Streamlit interface allows users to upload PDFs, input questions, and view bot responses.
- **Session Management**: Utilizes `st.session_state` in Streamlit to manage conversation history (`chat_history`) and maintain the current state of the conversation (`conversation`).

## Challenges and Solutions :warning:

- **PDF Handling**: Managing multiple PDF uploads and extracting meaningful text content posed initial challenges, resolved through robust handling in PyPDF2.
  
- **Model Integration**: Integrating and fine-tuning conversational models like OpenAI's GPT-3 for accurate and contextually relevant responses required careful setup and configuration within LangChain.
  
- **Performance**: Addressing response time and system performance considerations, especially with larger PDFs and complex queries, involved optimizations in text processing and model inference.

## Future Enhancements :rocket:

- **Performance Improvements**: Further optimize text extraction, vectorization processes, and model inference for enhanced speed and efficiency.
  
- **User Experience**: Enhance the interface for improved usability and engagement, potentially integrating features like document summarization or highlighting relevant passages.
  
- **Model Selection**: Explore and integrate different conversational models or embeddings to improve accuracy and response quality based on user feedback and ongoing research.
