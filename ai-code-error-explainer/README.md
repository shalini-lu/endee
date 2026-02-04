🤖 AI Code Error Explainer

A Semantic Search–Based Error Understanding System

Overview

AI Code Error Explainer is a semantic search–based application designed to help developers understand programming errors using natural language input.

Instead of relying on exact error names or keyword matching, this project uses vector embeddings to capture the meaning of an error description and retrieve the most relevant explanations across multiple programming languages.

The project is built as a practical AI/ML use case demonstrating how vector databases and semantic similarity can be applied to real-world developer problems.


Key Capabilities

Semantic search using vector embeddings

Natural language error input (no exact keywords required)

Top-3 ranked error matches with confidence interpretation

Cross-language support (Python, Java, C++, SQL)

Interactive web interface using Streamlit

Lightweight and fast local execution

System Architecture

The project follows a simple but effective pipeline:

Error Knowledge Base
A curated set of programming errors with explanations and fixes.

Vector Embedding Generation
Each error description is converted into a numerical vector using a pre-trained sentence embedding model.

Similarity Search
User input is embedded and compared against stored vectors using cosine similarity.

Ranking & Interpretation
Results are ranked by similarity and presented with human-readable confidence levels.

User Interface
A Streamlit-based UI allows users to interact with the system easily.

Technology Stack

Python 3

Sentence Transformers – semantic text embeddings

Scikit-learn – cosine similarity computation

Streamlit – interactive UI

Endee – vector database concept and integration reference

Endee Integration Context

This project is developed inside a forked Endee repository and follows vector database principles inspired by Endee’s architecture.

While Endee itself is a high-performance C++ vector database engine, this project focuses on:

Demonstrating how vector embeddings are generated

How similarity-based retrieval works

How such workflows integrate conceptually with a vector database system like Endee

Example Usage

User Input (Natural English):

my program crashes when accessing array index


System Output (Top Matches):

Java – ArrayIndexOutOfBoundsException

C++ – Segmentation Fault

Python – IndexError

This demonstrates semantic understanding across different languages and error types.

Running the Project
Prerequisites

Python 3.10+

Virtual environment recommended

Installation
python -m venv venv
source venv/bin/activate

pip install sentence-transformers scikit-learn streamlit

Running the Application
streamlit run app.py


The application will be available in the browser at:

http://localhost:8501


Project Structure
ai-code-error-explainer/
│
├── app.py                 # Streamlit UI
├── embeddings.py          # Embedding generation logic
├── explain_error.py       # Semantic search logic
├── store_errors.py        # Error ingestion
├── data/
│   └── errors.txt         # Error knowledge base
└── README.md

Design Decisions

Semantic similarity over keyword matching to improve usability

Confidence labels instead of raw similarity scores for better user understanding

Deferred model loading to ensure fast UI rendering

Simple architecture to clearly demonstrate vector search concepts
