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

  
