# RAG-fromScratch

👨🏻‍💻 The Python notebook contains both code and notes produced during <a href="https://youtu.be/qN_2fnOPY-M?si=nhuguHBT04HxDOfc">this</a> Daniel Bourke YouTube lesson. The main focus here was *not* to produce an optimized and scalable RAG pipeline, but rather to build intuition behind the core RAG process—without using frameworks such as LangChain or LlamaIndex, just Python with minimal tools.

By building this RAG pipeline from scratch, I was able to work with PDF loading and preprocessing, embedding models, similarity search, running an LLM locally, and prompt augmentation.

Key test-and-try points learned that are crucial for a good RAG pipeline:

- Choose a good embedding model and check if it was trained in the desired language(s). Also, check if a small embedding model works well, as it results in a faster pipeline and less storage.  
- If your RAG pipeline is mainly to summarize and structure the relevant pieces of text, you definitely don’t need a big model—start with a small one (< 10B).  
- Writing a good final prompt is a crucial part (some useful resources: <a href="https://www.promptingguide.ai/pt/introduction/examples">Prompting Guide</a>, <a href="https://github.com/brexhq/prompt-engineering">Brex’s Prompt Engineering Guide</a>, <a href="https://arxiv.org/abs/2401.14423">Related arXiv Paper</a>).  

Feel free to check out the notebook!

## Executing

To use the notebook, make sure to create a Python virtual environment and install the dependencies listed in `requirements.txt`. You also need to create a `.env` file, which must contain your Hugging Face API key in the `HF_TOKEN` field.
