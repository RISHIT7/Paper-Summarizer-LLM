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
   - **Broad Training Scope**: Large Language Models (LLMs) are trained on expansive and diverse datasets to comprehend and generate human language effectively. It often leads to responses that may lack the depth and specificity required in specialized fields. This generalist approach can also result in the generation of *"hallucinated"* content—responses that appear accurate and plausible but are factually incorrect or misleading.
   - **Insufficient Domain Expertise**: For domain-specific queries, such as technical documentation or niche knowledge areas, LLMs may fail to deliver precise and accurate responses, leading to generic or inaccurate answers.
 
## The RAG Approach 
RAG combines the strengths of information retrieval systems with the generative abilities of Large Language Models (LLMs) to produce more accurate and contextually relevant responses.
### A) Retrieval : 
* #### Retrievers :
  - **Function**: Identify and retrieve relevant data from external sources or databases based on the input query.
  - **Mechanism**: Use algorithms to search through vast collections of documents or data to find the most pertinent information .
  - **Types**:
    * ***Dense Retrievers***: Use neural embeddings to understand semantic similarity (e.g., BERT-based retrievers).
    * ***Sparse Retrievers***: Use traditional keyword-based methods (e.g., TF-IDF or BM25).
      
* #### Rankers :
  - **Function**: Evaluate and rank the retrieved documents or data segments based on their relevance to the query.
  - **Mechanism**: Apply scoring algorithms to prioritize the most relevant information.

### B) Augmentation : 
To augment means to add something .
- Herein , we enhance the raw input data ( retrieved from documents provided ) with additional information or context to improve the preformance of language models during the query generation process.
- The raw data is enriched by combining the user query with the retrieved content to create a more informaive input for the language model

### C) Generation :
- Use the retrieved information and query to draft a comphrehensive response . It analyses the key points and context from the retrieved information .
- The language models may personalize the response based on intent ( sarcastic , poetic ) or context.


For more detailed explanation about RAGs , feel free to go through this [Research Paper](https://arxiv.org/pdf/2312.10997) 
