# Module 8: RAG II — Evaluation and Improvement

Prepare PDF text for a RAG knowledge base. Use Gemma 3 to answer questions and check claims, then inspect passages, citations, and missing information.

## Contents

| File | Description |
| --- | --- |
| [`DSA495-M08-PDF-to-Text.ipynb`](./DSA495-M08-PDF-to-Text.ipynb) | Convert the M08 PDFs to TXT files and check extraction quality; CPU runtime. |
| [`DSA495-M08-RAG-Gemma3.ipynb`](./DSA495-M08-RAG-Gemma3.ipynb) | RAG workflow, evidence and answer checks, and optional retrieval plots. |

## Before You Begin

For PDF conversion, use a **CPU runtime** and the four course PDFs in `M08_RAG02`; edit `pdf_folder` to match your Drive folder.

For Gemma RAG, use a **T4 GPU**, accept Gemma's Hugging Face terms, and save a read token as `HF_TOKEN` in Colab Secrets. Set `KB_DIR` to the Module 7 TXT collection or your converted M08 TXT folder. Internet access is required. Run notebook cells in order.
