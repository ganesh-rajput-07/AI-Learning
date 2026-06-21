# Day 01 

### First lets set up the AI-LAB

1. we needs to have some libs, listed into the requirements.txt using uv

```
# install uv if not already there

curl -LsSf https://astral.sh/uv/install.sh | sh


# install python 3.12 for compatibility

uv python install 3.12


# create env if you want (Optional)

uv venv --python 3.12 ai-env


# now install requirements.txt 

pip install -r requirements.txt

# now create the required folders (Optional)

mkdir agents
mkdir experiments
mkdir notebooks
mkdir "rag-projects"
```


After performing above steps we just set up the LAB

___

## Learning topics for Today: (LLM Fundamentals)

* What is an LLM ?
* Difference between AI, ML, Deep Learning and LLM
* Why GPT is called a Language Model
* Why isn't it just a huge if-else statement ?
* What is Token ?
* What is a Tokenizer ?
* What is Context Window ?
* Why ChatGPT forgets older messages.
* Why GPT-4 can remember more than GPT-3.5.
* What is temperature ?
* What is Top-p ?
* Why does an LLM predict the **next token** instead of the next sentence?
* Why can't an LLM be implemented as a giant `if-else` program?
* What is the difference between a **word** and a **token**?
* Why does an LLM need a tokenizer?
* Why does a larger context window help with long conversations?
* If you increase temperature, what changes—and what does **not** change?
* How is top-p different from temperature?

(Just clear the concept not Rote learning)

## Coding part

- run the sh script if you set up or open the jupyter notebook if you have properly installed everything.
and use the Day-#01.ipynb.

