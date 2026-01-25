# Testing RAG and MLModels
I created this repository as a general knowledge base for anyone who needs to learn how to test AI Model.
Contents of this repo came from the knowledge that I acquired for RAG and Model validation as part of my job routine.

To build RAG, I’ll need the following libraries at minimum:
- from langchain.document_loaders import TextLoader
- from langchain.text_splitter import CharacterTextSplitter
- from langchain.vectorstores import Chroma
- from langchain.embeddings import HuggingFaceEmbeddings
- from langchain.chains import RetrievalQA
- from langchain.prompts import PromptTemplate
- from langchain.chains import ConversationalRetrievalChain
- from langchain.memory import ConversationBufferMemory

Besides the above libraries, I’ll need to gather the following:
1.	Document guideline
2.	Indexing the tokens from the above document: Embedded and store the data in Chroma DB
3.	Build parameters and model using pre-trained LLM
4.	Build PromptTemplate and memory
5.	Integrate the above model, promptTemplate, and memory with LangChain
6.	Create ConversationalRetrievalChain
7.	Build an agent

In order to validate the ML Model, I'll utilize LangChain and PromptTemplate.  I'll create LCEL for the model validation.
The following libraries need to be imported before we invoke the methods: 
- from langchain_core.prompts import PromptTemplate
- from langchain_core.runnables import RunnableLambda
- from langchain_core.output_parsers import StrOutputParser
- from langchain_core.runnables import RunnablePassthrough

Then LLM, parameters, template, and prompt need to be initialized prior to building LCEL 

### For custom application, I'll use tools and agents.
In order to use Tools and agents, you'll need to import the following libraries:
- from langchain_core.tools import Tool
- from langchain.tools import tool
- from langchain_core.prompts import PromptTemplate
- from langchain_core.prompts import ChatPromptTemplate, MessagesPlaceholder
- from langchain_core.messages import AIMessage, HumanMessage, SystemMessage
- from langchain.agents import create_react_agent, AgentExecutor

Then create tool using Tool class.  Note that we can create custom tool using @tool decorator

First, we'll initialize llm with the selected pretrained model, then create tools, create prompt template, create agent (using create_react_agent with llm, tools, and prompt template as parameters), then create agent executor

For testing, I'll use langchain-tests (for unit and integration tests), LLM-as-Judge, and LangSmith
### How to properly test Similarity Search on Vector DB?
### How to test Recommendation system?

# LangChain Context Retrieval

I'll add examples as I move forward with building the custom application 

## Remark:  I'll continue to update this repo with more contents...
