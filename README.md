![SimonChat](./image/SimonChat.png)
# Installation
We provide an interactive tool based on `Gradio`, which requires the installation of `gradio`, `openai`, and `spacy`.

```shell
pip install -r requirements.txt
python -m spacy download en_core_web_md
```
# API
We utilize the API of Yi-chat-34B to implement interaction based on Large Language Models (LLMs). Therefore, you need to create a `.env` file in advance to set the `API KEY` and `API BASE`.
```python
from dotenv import load_dotenv

load_dotenv("info.env", override=True)
API_BASE = os.getenv("API_BASE")
API_KEY = os.getenv("API_KEY")
```
# Highlights

1. Our summary hallucination process is integrated with an interactive interface, `SimonChat`, which streamlines the manual oversight and annotation of factual inconsistencies within abstractive summaries, enhancing the efficiency of the review process.

2. Acknowledging the token-intensive nature and slower detection speeds associated with most Large Language Model (LLM)-based methods, we have adopted a strategy that employs universal information extraction (UIE).  This approach efficiently captures key details from both the document and the summary, facilitating a more rapid and accurate comparison and verification of factual discrepancies.

3. Our designed framework supports an iterative approach to rectifying erroneous summaries. It prioritizes the correction of `entity-related errors` before addressing `logical inconsistencies`, ensuring a systematic and comprehensive enhancement of summary accuracy.
