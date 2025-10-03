Simple RAG Pipeline
This project is a beginner-friendly tutorial project for building a Retrieval Augmented Generation (RAG) system. It demonstrates how to index documents, retrieve relevant content, generate AI-powered responses, and evaluate results—all through a command line interface (CLI).


Overview
The RAG Framework lets you:

Index Documents: Process and break documents (e.g., PDFs) into smaller, manageable chunks.
Store & Retrieve Information: Save document embeddings in a vector database (using LanceDB) and search using similarity.
Generate Responses: Use an AI model (via the OpenAI API) to provide concise answers based on the retrieved context.
Evaluate Responses: Compare the generated response against expected answers and view the reasoning behind the evaluation.
Architecture
Pipeline (src/rag_pipeline.py):
Orchestrates the process using:

Datastore: Manages embeddings and vector storage.
Indexer: Processes documents and creates data chunks. Two versions are available—a basic PDF indexer and one using the Docling package.
Retriever: Searches the datastore to pull relevant document segments.
ResponseGenerator: Generates answers by calling the AI service.
Evaluator: Compares the AI responses to expected answers and explains the outcome.
Interfaces (interface/):
Abstract base classes define contracts for all components (e.g., BaseDatastore, BaseIndexer, BaseRetriever, BaseResponseGenerator, and BaseEvaluator), making it easy to extend or swap implementations.
