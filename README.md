# How Deep Agents Remember Without Keeping Everything in Context

Slides and demo notebook for the talk of the same name, part of the O'Reilly Agent Memory Expert Showcase.

The talk covers three ways a deep agent keeps working on a task without dragging every past token along with it:

- **Offloading** — oversized tool results are written to the filesystem instead of staying in context.
- **Subagents** — noisy work runs in its own isolated context and only reports back a distilled answer.
- **Summarization** — a long-running conversation gets compacted once it crosses a token threshold, without losing what matters.

Long-term memory (an agent remembering things across entirely separate conversations) is a different topic and isn't covered here.

## Contents

- `How Deep Agents Remember Without Keeping Everything in Context.pptx` — the talk slides.
- `memory_demo.ipynb` — a runnable companion notebook. One scenario (a market-intelligence agent drafting a company briefing) demonstrates all three mechanisms in sequence.

## Running the notebook

1. Open `memory_demo.ipynb` in Jupyter or VS Code.
2. Run the setup cell to install dependencies (`deepagents`, `langgraph`, `langchain-anthropic`, `faker`, `python-dotenv`).
3. Add an Anthropic API key to a local `.env` file in this directory:
   ```
   ANTHROPIC_API_KEY=sk-ant-...
   ```
4. Run the remaining cells top to bottom.

The notebook runs end to end in under 15 minutes.

## More

For long-term memory, backends, skills, sandboxes, and deployment, see the self-paced [LangChain Academy Deep Agents course](https://academy.langchain.com/).
