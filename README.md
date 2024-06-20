# RAG Application from Scratch

This repository contains a step-by-step guide to building a simple RAG (Retrieval-Augmented Generation) application using the LangChain framework and OpenAI's API. This application allows users to ask questions about any YouTube video by converting the video into a transcript and then querying the transcript with the help of RAG and LLM functionality.

## Overview

The notebook demonstrates how to build an application that:

1. Reads a YouTube video.
2. Converts the video into a transcript.
3. Processes and embeds the transcript.
4. Allows users to query the transcript using an LLM.

## Steps Involved

1. **Create an OpenAI API Key**
   - Generate an API key to be used for GPT-3.5-turbo.

2. **Functionalities Used from LangChain**
   - **Output Parsers**
     - `StrOutputParser`: Formats the output of the LLM.
   - **Prompt Templates**
     - `ChatPromptTemplate`: Creates templates for querying the LLM.
   - **Chaining Functionality**
     - Chains together different functions to get the output.
   - **YouTube Video Processing**
     - Uses `whisper` and `pytube` to read a YouTube video and create a transcript.
   - **Transcript Processing**
     - Loads the transcript, divides it into small chunks, and embeds it using LangChain functions such as:
       - `langchain_openai.embeddings`
       - `DocArrayInMemorySearch`
       - `RunnableParallel`
       - `RunnablePassthrough`
   - **Saving Vector Store Locally**
     - Uses LangChain function `FAISS` to save the vector store locally.

## Requirements

- Python 3.7+
- LangChain
- OpenAI's API key
- whisper
- pytube
- faiss-cpu

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/rag-application.git
   cd rag-application
