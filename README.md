# Paper-Summarizer-Bot
The usual Generative Approach for dealing with outcomes involves the following series of steps : 
* ### External Data Source:
  - **Data Collection**: Gather data from various web sources using APIs or web scrapers.
  - **Storage**: Use SQL or NoSQL databases to store the structured data.
  - **Pre-processing**: Employ Python libraries for cleaning and preparing the data for further processing.
    
* ### Embedding Models :
  - **Data Types**: The collected data may include text, images, or videos.
  - **Conversion to Numerical Data**: Transform the raw or preprocessed data into vector embeddings. This conversion captures semantic relationships between elements and encodes them in a numerical vector form.
  - **Tools**: Utilize transformers like BERT, GPT, and Sentence Transformers (available via Hugging Face) to generate these embeddings.
    
* ### Large Language Models :
  - **Input to LLMs**: Feed the vector embeddings into pre-trained LLMs.
  - **Model Choices**: Use models from the GPT series or LLaMA series for processing the embeddings to generate meaningful outcomes.
 
## Introduction To Retrieval Augmented Generation (RAGs) 
While generative approaches using Large Language Models (LLMs) like GPT or LLaMA have revolutionized natural language processing, they are not without their limitations.  
* ### Static Knowledge Base:
  - **Outdated Information**: LLMs are trained on large, but static datasets. Consequently, they cannot update or acquire new information after their training phase, making them unsuitable for tasks requiring the latest or dynamically changing data.
  - **Lack of Real-time Context**: Without real-time data access, these models struggle to provide up-to-date answers, particularly in rapidly evolving domains.
* ### Generic Responses
   - **Broad Training Scope**: LLMs are trained on vast and diverse datasets to understand and generate language. However, this generalist training often results in responses that lack specificity and depth in specialized fields.
   - **Insufficient Domain Expertise**: For domain-specific queries, such as technical documentation or niche knowledge areas, LLMs may fail to deliver precise and accurate responses, leading to generic or inaccurate answers.
 
## The RAG Approach 
RAG combines the strengths of information retrieval systems with the generative abilities of Large Language Models (LLMs) to produce more accurate and contextually relevant responses.
* ### Retrievers :
  - **Function**: Identify and retrieve relevant data from external sources or databases based on the input query.
  - **Mechanism**: Use algorithms to search through vast collections of documents or data to find the most pertinent information .
  - **Types**:
    * ***Dense Retrievers***: Use neural embeddings to understand semantic similarity (e.g., BERT-based retrievers).
    * ***Sparse Retrievers***: Use traditional keyword-based methods (e.g., TF-IDF or BM25).
      
* ### Rankers :
  - **Function**: Evaluate and rank the retrieved documents or data segments based on their relevance to the query.
  - **Mechanism**: Apply scoring algorithms to prioritize the most relevant information.

* ### LLMs :
  - **Role in RAG**: Generate responses by appending retrieved data embeddings to their pre-trained knowledge.
  - **Integration**: Instead of training the LLM on the entire dataset, the RAG approach appends embeddings of the retrieved information to enhance the model's responses dynamically.
