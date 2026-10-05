# Module 8: RAG II — Evaluation and Improvement

Adapted from Serena Kim's Module08 course notebooks to load course inputs directly from this GitHub repository.

| File | Purpose | Runtime |
| --- | --- | --- |
| [PDF-to-Text](DSA495-M08-PDF-to-Text.ipynb) | Download the four Module08 PDFs from GitHub, convert to TXT, inspect extraction quality. | CPU |
| [RAG with Gemma 3](DSA495-M08-RAG-Gemma3.ipynb) | Download the matching TXT files from GitHub, retrieve passages, generate cited answers, inspect retrieval plots. | T4 GPU |

The RAG notebook defaults to `KB_COLLECTION = "M08_RAG02"`; set it to `"M07_RAG01"` for the original renewable-energy TXT activity. No Google Drive mounting is required.

**All four Module08 PDFs and extracted TXT files are included.** See [data status and source folders](../data/README.md). The notebooks stop with an actionable message if inputs are missing.

For Gemma, accept the [model terms](https://huggingface.co/google/gemma-3-4b-it) and store a Hugging Face read token as `HF_TOKEN` in Colab Secrets. Run cells in order. [Colab links and course readings](../README.md).


## Interactive document explorer

[Open the Module08 HTML page](https://htmlpreview.github.io/?https://github.com/StrokeOfLuck/DSA495-Module08-Rag/blob/main/index.html) to type questions, inspect exact source passages, and work through the notebook activities. [Repository overview](../README.md).
