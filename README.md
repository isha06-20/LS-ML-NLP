# LS-ML-NLP
This repo contains my weekly assignments, notes and projects completed as part of Wncc Machine learning Learners Space.

# IITB Insti Assist: A RAG Powered AI Assistant for IIT Bombay

## Overview

IITB Insti Assist is a Retrieval Augmented Generation (RAG) based AI assistant developed to answer questions about IIT Bombay using official institute documents. Unlike a generic Large Language Model (LLM), this assistant retrieves relevant information from a curated knowledge base before generating a response, ensuring that answers are grounded in official documentation rather than model memory.

The assistant is designed to answer academic and institute related queries while refusing to answer questions that are not supported by the available documents.


## Features

- Retrieval Augmented Generation 
- Semantic document search using sentence embeddings
- FAISS vector database for fast similarity search
- Grounded responses generated using Google Gemini
- Source document and page citation for every answer
- "I don't know" response when sufficient evidence is unavailable
- Interactive web interface built using Gradio


## Project Architecture


User Question
      │
      ▼
Generate Query Embedding
      │
      ▼
FAISS Vector Search
      │
      ▼
Retrieve Top k Relevant Chunks
      │
      ▼
Prompt Construction
      │
      ▼
Google Gemini LLM
      │
      ▼
Grounded Answer + Sources



## Dataset

The knowledge base consists of official IIT Bombay academic documents including:

- Undergraduate Rule Book
- Policy Newsletters
- Fast Track Degree Guide
- Academic Procedure Documents
- Rejoining Procedures
- Other official academic documents

Total Documents: **9**

Total Pages: **98**

Total Chunks: **170**

Embedding Dimension: **384**



## Technology Stack

| Component | Technology |
|-----------|------------|
| Programming Language | Python |
| PDF Parsing | PyPDF |
| Text Embedding | Sentence Transformers (all-MiniLM-L6-v2) |
| Vector Database | FAISS |
| Large Language Model | Google Gemini |
| User Interface | Gradio |



## Project Structure


IITB Insti Assist/
│
├── app.py
├── README.md


## How it works

1. Official IIT Bombay PDF documents are loaded.
2. Documents are divided into overlapping chunks.
3. Each chunk is converted into a semantic embedding using Sentence Transformers.
4. Embeddings are stored in a FAISS vector database.
5. When a user asks a question:
   - the query is embedded,
   - the most relevant document chunks are retrieved,
   - retrieved context is injected into the prompt,
   - Gemini generates an answer using only the retrieved information.
6. The assistant displays both the answer and the supporting source documents.


## Limitations

- Limited to uploaded IIT Bombay documents.
- Cannot answer questions outside the available knowledge base.
- Performance depends on document quality and retrieval accuracy.
- Does not maintain multi-turn conversational memory.



## Future Improvements

- Chat history and conversational memory
- PDF upload by users
- Confidence score for retrieved answers
- Highlight retrieved text passages
- Hybrid keyword + semantic search
- Support for additional IIT Bombay departments and councils


## Authors

Developed as the Final Project for the **WnCC NLP Learners' Space** at **IIT Bombay**.


## License

This project is intended for educational purposes.

### WEEKLY ASSIGNMENTS DONE BEFORE COMPLETING PROJECT 

## Week 1 
### Assignment
|Q1|https://colab.research.google.com/drive/1pnAHRzcRbHgrn9kJxm5sGWR6c5o5LGnt?usp=sharing |
|Q2|https://colab.research.google.com/drive/1JVExOQJr3YmnKq5UFFbmth5hLu2iD7Ub?usp=sharing|
## Week 2 
### Assignment 
|Q1|https://colab.research.google.com/drive/1xqCsp4SEi8jhczlaOfv6eulIDoA8C_j2?usp=sharing|

## Topics covered 

### week 1 
- python basics
- NumPy
- Data Analysis

### week 2
- NLP preprocessing
- Bag of Words
- TF-IDF
- LOgistic Regression
- MLP using PyTorch

  
