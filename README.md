# README

This is a database of items from a store captioned by a llm.

## Install

Be in the parent directory of this repository.

```powershell
ollama pull phi3:medium-128k
ollama pull nomic-embed-text:v1.5
ollama serve
```

```
scoop install python
# Install microsoft visual studio on the pc.
pip3 install git+https://github.com/s106916/graphrag@json_fix
# python -m graphrag.index --root . --init
# Resume from an earlier snapshot
# python -m graphrag.index --root . --resume 20240712-031618
python -m graphrag.index --root .
# Tune prompts for better results
# python -m graphrag.prompt_tune --root . --no-entity-types
```

## Global SearchExample

```powershell
python -m graphrag.query --data .\omigroup\output\20240712-031618\artifacts\ --community_level 3 --response_type "Multiple Paragraphs" --method "local" "Can you provide recommendations for items to purchase from the virtual market based on user preferences and past purchase history? Please include a high-level summary of why each item is recommended, highlighting key features and benefits. Additionally, can you suggest complementary products that would enhance the user's experience with their primary purchases? If possible, outline any ongoing promotions or discounts that could be advantageous for the user."
```
