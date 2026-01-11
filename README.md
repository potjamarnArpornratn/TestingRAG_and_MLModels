# TestingMLModels
I created this repository as a general knowledge base for anyone who needs to learn how to test AI Model.
Contents of this repo came from the knowledge that I acquired for Model validation as part of my job routine.

In order to validate the ML Model, I'll utilize LangChain and PromptTemplate.  I'll create LCEL for the model validation.
The following libraries need to be imported before we invoke the methods: 
- from langchain_core.prompts import PromptTemplate
- from langchain_core.runnables import RunnableLambda
- from langchain_core.output_parsers import StrOutputParser

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

I'll add examples as I move forward with building the custom application 

## Remark:  I'll continue to update this repo with more contents...
