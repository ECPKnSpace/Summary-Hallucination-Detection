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
