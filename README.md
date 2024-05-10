# Agentic-RAG-with-LLAMAIndex

This repo contains code from the deeplearning.ai course https://www.deeplearning.ai/short-courses/building-agentic-rag-with-llamaindex/ and self-made projects around the learnings from the course.

**Module 1** - [Router Query Engine](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5D%20L1_Router_Engine.ipynb) 

This module covers the Router query engine, featuring a vector index(returns similar nodes only) and summary index(returns all nodes). It covers conversion from Indexes to Query Engines to Query tools using llmaa_index_core.tools. Final Router Query Engine selection is made using an LLM selector that uses LLM to output a JSON that is parsed and corresponding indexes are queried.

**Module 2** - [Tool Calling](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5DL2_Tool_Calling.ipynb)

This module covers tool calling which enables LLMs to interact with external environments through dynamic interface by choosing appropriate tools and inferring necessary arguments for execution. It adds a layer of query understanding that enables users to ask complex queries and get more precise results. It also covers Auto Retrieval tool where we use MetadataFilters to filter out response as per metadata such as page number, header, footer, etc.

-----------------------------------------------------------------------------------------------------
## **Requirements:**

Running [COURSE] code requires OPENAI API Key and some helper functions defined in **utils.py** along with the following:

python-dotenv==1.0.0

llama-index==0.10.27

llama-index-llms-openai==0.1.15

llama-index-embeddings-openai==0.1.7
