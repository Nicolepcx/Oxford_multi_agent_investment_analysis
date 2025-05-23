# Oxford Multi-agent Investment Analysis

This is the code for the session "Multi-Agent-Workflow for Investment Analysis" for Agentic Workflows: Design and Implementation (online). 

The code for the multi-agents draws inspiration from the paper [AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://arxiv.org/abs/2308.08155) by Wu et al., and from the [examples from LangGraph](https://github.com/langchain-ai/langgraph/tree/main/examples/multi_agent). 


You will find three notebooks which you can directly open in Google Colab:

- `Oxford_LangGraph_multi_agents_investment_analysis.ipynb`: This is the notebook to create a multi-agent investment report with LangGraph.
- `lats_advice.ipynb`: This is the notebook shown during the talk for creating LATS.
- `Oxford_langgraph_multiturn_conversation.ipynb`: Multi-turn Human-in-the-Loop conversation with LangGraph


## Multi-Agent Investment Analysis


For the multi-agents, you will use the following tools:

  - [Exa](https://exa.ai/search), after account login, get your [API key here](https://docs.exa.ai/reference/getting-started-with-python). To find the exact content you're looking for on the web using embeddings-based search.  
  - [SerpApi here](https://serpapi.com/), after account login, get your [API key](https://serpapi.com/dashboard) to do look for existing patents.
  - [Python REPL](https://python.langchain.com/docs/integrations/tools/python/), please note that Python REPL can execute arbitrary code on the host machine (e.g., delete files, make network requests). Use with caution.
  - A finetuned [LLM from HuggingFace](https://huggingface.co/mrm8488/distilroberta-finetuned-financial-news-sentiment-analysis) for sentiment anylysis
  - Tools to access and write to a `.txt` file and create a plot of historical prices.
- How to define utilities to help create the graph.
- How to create a team supervisor and the team of agents.


The interaction of the multi-agents looks like this:

![graph.jpeg](resources%2Fgraph.jpeg)

## Language Agent Tree Search

[Language Agent Tree Search](https://arxiv.org/abs/2310.04406) (LATS), by Zhou, et. al, is a general LLM agent search algorithm that combines reflection/evaluation and search (specifically monte-carlo trees search) to get achieve better overall task performance compared to similar techniques like ReACT, Reflexion, or Tree of Thoughts:

![LATS.jpg](resources%2FLATS.jpg)
