# YT-live-chat-sentiment-analysis
A Python script that streams live YouTube chat messages and runs them through a multilingual sentiment analysis model using Hugging Face Transformers.   This lets you see the mood of a livestream audience in real time. No API or Log in required.
---
## Features
- Capture live chat messages from any YouTube livestream.
- Analyze sentiment (positive, negative, neutral) using a multilingual model.
- Limit the number of messages processed with a simple input.
- Display both the raw message and its sentiment classification.

## Requirements
- Python 3.10+
- [chat-downloader](https://pypi.org/project/chat-downloader/)
- [transformers](https://pypi.org/project/transformers/)
- A deep learning backend (PyTorch or TensorFlow). PyTorch is recommended.
- A link from a LIVE youtube livestream

## Install dependancies
```bash
pip install chat-downloader@git+https://github.com/Indigo128/chat-downloader
pip install transformers torch
```

# Usage
Run the script:
```bash
python YTsentimentchecker.py
```
Paste the YouTube livestream URL when prompted, then enter how many messages you want to analyze.

```bash
Paste url of live livestream (YT): https://www.youtube.com/watch?v=jfKfPfyJRdk
How many messages do you want to see the result of: 5
```
Output (example):
```bash
wow, [{'label': 'positive', 'score': 0.98}]
video se traba, [{'label': 'negative', 'score': 0.87}]
lol, [{'label': 'positive', 'score': 0.67}]
formidable, [{'label': 'positive', 'score': 0.95}]
thanks, [{'label': 'positive', 'score': 0.99}]
```
## ⚠️Note
- `chat-downloader` is not officially supported by YouTube and may break when YouTube updates its site.
- Some livestreams do not have chat replay enabled, which can cause parsing errors.
- The script may work intermittently; if it fails, try `pip install --upgrade --force-reinstall chat-downloader@git+https://github.com/Indigo128/chat-downloader`, and keep re-running the script.
