
# LangChainWithOpenRouter

This project is an implementation of LangChain with ([OpenRouter](https://openrouter.ai/docs#models)). It uses the OpenRouter AI API to interact with Large Language Model (gryphe/mythomist-7b). The project also includes functionality for loading documents from YouTube and the web, splitting text into manageable chunks, embedding these chunks using HuggingFace embeddings, and storing these embeddings in a FAISS vector store for efficient retrieval.

## Obtaining API Token

To interact with the Free Large Language Model (gryphe/mythomist-7b) via OpenRouter, you will need an API token. OpenRouter provides free API tokens for developers. 

Follow these steps to obtain your free API token:

1. Visit the [OpenRouter website](https://openrouter.ai/).
2. Click on the "Sign in" button.
3. After logging in, Click on the "Account" button. then select "Keys" navigate to the "API Tokens" section.
4. Click on "Create Key".
5. Copy the generated token and store it safely. You will not be able to view the token again.

Once you have the token, you need to add it to your `.env` file:

```bash
OPENAI_API_KEY=your_api_key_here
```

## Getting Started

These instructions will get you a copy of the project up and running on your Google Colab (CPU) for development and testing purposes.

### Prerequisites

You need to install the following Python packages:

- langchain
- langchain-openai
- faiss-cpu
- tiktoken
- youtube-transcript-api
- pytube
- python-dotenv
- sentence-transformers

You can install them using pip:

```bash
pip install --upgrade --quiet  langchain langchain-openai faiss-cpu tiktoken
pip install youtube-transcript-api  pytube --quiet
pip install python-dotenv --quiet
pip install sentence-transformers --quiet
```


### Usage

the following tasks:

1. Loads a YouTube video transcript or a webpage.
2. Splits the loaded document into chunks.
3. Embeds these chunks using HuggingFace embeddings.
4. Stores these embeddings in a FAISS vector store.
5. Retrieves relevant chunks based on a given question.
6. Sends the retrieved chunks and the question to the Large Language Model to generate a response.

You can modify the script to use different models, change the chunk size, or adjust the number of retrieved chunks.

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
