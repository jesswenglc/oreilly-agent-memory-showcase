# How Deep Agents Remember Without Keeping Everything in Context

Three ways a deep agent avoids holding every past token in context:

- **Offloading**: oversized tool results are written to the filesystem instead of staying in context.
- **Subagents**: noisy work runs in its own isolated context and reports back only a distilled answer.
- **Summarization**: a long conversation gets compacted once it crosses a token threshold, without losing what matters.

The slides also cover long-term memory, remembering things across separate conversations. The notebook focuses on the three mechanisms above.

## Contents

- `How Deep Agents Remember Without Keeping Everything in Context.pptx`: the talk slides.
- `memory_demo.ipynb`: a runnable notebook. One scenario, a market-intelligence agent drafting a company briefing, demonstrates all three mechanisms.

## Running the notebook

1. Open `memory_demo.ipynb` in Jupyter or VS Code.
2. Run the setup cell to install dependencies (`deepagents`, `langgraph`, `langchain-anthropic`, `faker`, `python-dotenv`).
3. Add an Anthropic API key to a local `.env` file in this directory:
   ```
   ANTHROPIC_API_KEY=sk-ant-...
   ```
4. Run the remaining cells top to bottom.

Runs end to end in under 15 minutes.

## More

For backends, skills, sandboxes, and deployment, see the [LangChain Academy Deep Agents course](https://academy.langchain.com/).
