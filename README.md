# Question-AnsweringOnDocuments
QA on documents with LangChain framework and Hugging Face LLM and prompt Templates

LangChain is a framework designed to simplify the creation of LLM applications. The core building block of LangChain applications is LLMChain. This is combined with-
1. Large Language Model - is the core engine
2. Prompt templates - provide instructions to the language model
3. Output parser - These translate the raw output from LLM


For LLM, I use Hugging Face API to access the model. The procedure of my project:
1. Load the document
2. Split the document into chunks for embedding and vector store
3. Sentence_transformer used for embedding.  Find more in SBERT.net
https://lnkd.in/eZNVEu_6
4. According to my query, similarity_search is done based on VectorStore or db and query. This is to find out the lowest distanced embedded chunks.
5. Load the LLM from HuggingFaceHub
6. for LLMChain input the lowest distanced embedded chunks with LLM,
7. For proper answers, try different models, used for specific tasks. (eg: texttotext) 
