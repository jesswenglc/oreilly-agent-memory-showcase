# How Deep Agents Remember Without Keeping Everything in Context

## Slides

`How Deep Agents Remember Without Keeping Everything in Context.pptx`

Covers:

- **Offloading**: oversized tool results are written to the filesystem instead of staying in context.
- **Subagents**: noisy work runs in its own isolated context and reports back only a distilled answer.
- **Summarization**: a long conversation gets compacted once it crosses a token threshold, without losing what matters.
- **Skills**: packaged instructions and tools a deep agent loads into context only when needed.
- **Long-term memory**: remembering things across separate conversations.

## Notebook

`memory_demo.ipynb`

A runnable demo of offloading, subagents, and summarization, using one scenario: a market-intelligence agent drafting a company briefing.

### Running the notebook

1. Open `memory_demo.ipynb` in Jupyter or VS Code.
2. Run the setup cell to install dependencies (`deepagents`, `langgraph`, `langchain-anthropic`, `faker`, `python-dotenv`).
3. Add your model API key to a local `.env` file in this directory (this notebook defaults to Anthropic, but feel free to use any model):
   ```
   ANTHROPIC_API_KEY=sk-ant-...
   ```
4. Run the remaining cells top to bottom.

Runs end to end in under 15 minutes.

## More

For backends, sandboxes, and deployment, see the [LangChain Academy Deep Agents course](https://academy.langchain.com/).
