# Agentic-RAG-with-LLAMAIndex

This repo contains code from the deeplearning.ai course https://www.deeplearning.ai/short-courses/building-agentic-rag-with-llamaindex/ and self-made projects around the learnings from the course.

**Module 1** - [Router Query Engine](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5D%20L1_Router_Engine.ipynb) 

This module covers the Router query engine, featuring a vector index(returns similar nodes only) and summary index(returns all nodes). It covers conversion from Indexes to Query Engines to Query tools using llmaa_index_core.tools. Final Router Query Engine selection is made using an LLM selector that uses LLM to output a JSON that is parsed and corresponding indexes are queried.

**Module 2** - [Tool Calling](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5DL2_Tool_Calling.ipynb)

This module covers tool calling which enables LLMs to interact with external environments through dynamic interface by choosing appropriate tools and inferring necessary arguments for execution. It adds a layer of query understanding that enables users to ask complex queries and get more precise results. It also covers the Auto Retrieval tool where we use MetadataFilters to filter out responses as per metadata such as page number, header, footer, etc.

**Module 3** - [Building an Agent Reasoning Loop](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5D%20L3_Building_an_Agent_Reasoning_Loop.ipynb)

This module covers an Agent Reasoning loop with memory to maintain chats. It makes use of two agents namely - an agent runner and an agent worker where the agent runner sees the overall tasks and orchestrates runs of the agent worker on top of a given task whereas the agent worker is responsible for executing the next step of the given agent.

**Module 4** - [Building_a_Multi-Document_Agent](https://github.com/AashiDutt/Agentic-RAG-with-LLAMAIndex/blob/main/%5BCOURSE%5DL4_Building_a_Multi-Document_Agent.ipynb)

This module covers two techniques to work with multiple documents. One for limited docs like 2-3 papers and one for a large number of documents like 100 papers. Initially both methods read documents and convert them into tools, then if the number of documents is small(say 2) then pass in the query to one of the 6 (2 tools per doc (vector tool and summary tool)) and get the response. Idf the number of documents is large say 11 documents then we use object retriever method. The object retriever method retrieves a small set of relevant tools and then feeds those relevant tools to the agent reasoning prompt instead of all calls thereby saving the cost of making too many calls and saving LLM from getting confused with too many tools to choose from.


-----------------------------------------------------------------------------------------------------
## **Requirements:**

Running [COURSE] code requires OPENAI API Key and some helper functions defined in **utils.py** along with the following:

python-dotenv==1.0.0

llama-index==0.10.27

llama-index-llms-openai==0.1.15

llama-index-embeddings-openai==0.1.7
