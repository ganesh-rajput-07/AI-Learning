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

