# Nemotron-RAG-Demo

Nemotron-RAG-Demo is a local implementation of a Retrieval-Augmented Generation (RAG) pipeline using the `nemotron-mini` model. The project demonstrates how to retrieve relevant information from documents and generate abstract responses to science and engineering-related queries. This demo leverages the `LangChain` framework and `Ollama` models for query processing and contextual answering.

## Features

- **Retrieval-Augmented Generation (RAG)**: Combines document retrieval with language model generation to provide comprehensive responses.
- **Nemotron-mini Model**: Utilizes the `nemotron-mini` language model for generating broad and conceptual answers.
- **Contextual Question Answering**: Focuses on answering science and engineering questions in a broad and abstract way.
- **Document Embeddings**: Implements a document retriever based on vector embeddings for efficient information retrieval.
- **PDF Document Loader**: Loads and splits a PDF document to extract relevant information.

## Requirements

- Python 3.9 or above
- LangChain
- Ollama Community package
- DocArray
- PyPDFLoader
- Other dependencies listed in the `requirements.txt`

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/peksikeksi/nemotron-rag-demo.git

2. Navigate to the project directory:

   ```bash
   cd nemotron-rag-demo

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt

4. Ensure you have the PDF file in the project directory

## How Retrieval-Augmented Generation (RAG) Works

Retrieval-Augmented Generation (RAG) is a hybrid approach that combines traditional retrieval-based methods with generative models. This architecture aims to improve the quality of generated responses by incorporating relevant external information into the generation process. Here’s a breakdown of how RAG operates:

### 1. **Retrieval Step**
The first step involves retrieving relevant documents or information based on a given query. This is typically done using:

- **Document Indexing**: The documents are indexed using embeddings, allowing for efficient searching.
- **Retriever**: A retriever queries the indexed documents to find relevant content that can help answer the user's question. In our implementation, we use the `DocArrayInMemorySearch` class to manage this process.

### 2. **Contextualization**
Once the relevant documents are retrieved, they provide context for the generative model. The retrieved content is used to inform the model's understanding of the query, ensuring that the responses are grounded in real data.

### 3. **Generation Step**
In this step, the generative model, which in our case is powered by the Nemotron-mini model, takes both the user query and the retrieved context to generate a coherent and contextually relevant answer. The model is prompted to answer broad questions, considering various perspectives based on the context provided.

### 4. **Output**
The final output is produced by the generative model, which synthesizes the information from the retrieved documents and responds to the user's question. The goal is to provide comprehensive and informed answers that leverage both the generative capabilities of the model and the factual grounding from the retrieved data.

### Advantages of RAG
- **Increased Accuracy**: By incorporating relevant external data, RAG models can generate more accurate and contextually appropriate responses.
- **Flexibility**: RAG models can adapt to a wide range of topics by simply updating the underlying document set.
- **Scalability**: This approach allows for scaling knowledge without retraining the model by simply adding new documents to the index.

Overall, RAG represents a significant advancement in natural language processing, effectively bridging the gap between retrieval and generation.

## References and Cool links
* Retrieval-Augmented Generation for Large Language Models: A Survey - https://arxiv.org/abs/2312.10997
* Improving the Domain Adaptation of Retrieval Augmented Generation (RAG) Models for Open Domain Question Answering - https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00530/114590/Improving-the-Domain-Adaptation-of-Retrieval
* Retrieval-Augmented Generative Agent for Scientific Research - https://arxiv.org/pdf/2312.07559
* Analytics Vidhya article - https://www.analyticsvidhya.com/blog/2023/09/retrieval-augmented-generation-rag-in-ai/
* Medium article - https://medium.com/@nidhikamewar1506/intro-to-retrieval-augmented-generation-rag-framework-b19b6a36b499
* Google Cloud article - https://cloud.google.com/use-cases/retrieval-augmented-generation
* AWS article - https://aws.amazon.com/what-is/retrieval-augmented-generation/
* IBM article - https://research.ibm.com/blog/retrieval-augmented-generation-RAG
* Langchain series - https://www.youtube.com/watch?v=wd7TZ4w1mSw&list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x
* Langchain-ai github page - https://github.com/langchain-ai/rag-from-scratch
* Integrating Retrieval-Augmented Generation with Large Language Models in Nephrology: Advancing Practical Applications - https://www.mdpi.com/1648-9144/60/3/445
* freeCodeCamp.org - https://www.youtube.com/@freecodecamp
* Take a Step Back: Evoking Reasoning via Abstraction in Large Language Models - https://arxiv.org/pdf/2310.06117
*  Underfitted - https://www.youtube.com/@underfitted
