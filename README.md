# DSA 495 — Module 08: RAG II

Sean Ryan's copy of the [Module08 course materials](https://github.com/SerenaYKim/DSA495-TextAnalysis/tree/master/Module08), taught by Serena Kim at NC State.

## Open the notebooks

| Notebook | View on GitHub | Run in Google Colab | Runtime |
| --- | --- | --- | --- |
| Convert PDFs to text | [PDF-to-Text](Module08/DSA495-M08-PDF-to-Text.ipynb) | [Open in Colab](https://colab.research.google.com/github/StrokeOfLuck/DSA495-Module08-Rag/blob/main/Module08/DSA495-M08-PDF-to-Text.ipynb) | CPU |
| Retrieve evidence and generate cited answers | [RAG with Gemma 3](Module08/DSA495-M08-RAG-Gemma3.ipynb) | [Open in Colab](https://colab.research.google.com/github/StrokeOfLuck/DSA495-Module08-Rag/blob/main/Module08/DSA495-M08-RAG-Gemma3.ipynb) | T4 GPU |

[Original Module08 instructions](Module08/README.md)

## Connect the course data

The instructor's Module08 GitHub folder contains **two notebooks and a README**. It does **not** contain the four course PDFs or the three Module 7 TXT files. All three GitHub files are copied here unchanged; the data must be supplied from the course materials in Google Drive.

| Data collection | Used by | How to connect it |
| --- | --- | --- |
| Four `M08_RAG02` PDFs, with filenames beginning `D00000`–`D00003` | PDF-to-Text notebook | Put the PDFs in My Drive, mount Drive, and change `pdf_folder` to that folder's path. |
| TXT files generated from those PDFs | Gemma RAG notebook, using the Module08 PDF collection | Set `KB_DIR` to the converter's printed `output_dir`: the `text` subfolder beside the PDFs. |
| Three Module 7 TXT files: Columbia, DOE, and EPA | Gemma RAG notebook's default renewable-energy activity | Put the course TXT files in `MyDrive/knowledgebase`, or change `KB_DIR` to their actual folder. |

For the **PDF → RAG workflow**:

1. Open PDF-to-Text in Colab with a CPU runtime.
2. Mount Drive and edit `pdf_folder`; the instructor's example path is `/content/drive/MyDrive/a-ncsu-courses/DSA495-2026/Data/M08_RAG02`.
3. Run the conversion and inspect the extracted text. The TXT files are saved beside the PDFs in `text/`.
4. Open Gemma RAG in a separate Colab notebook with a T4 GPU.
5. Accept the [Gemma model terms](https://huggingface.co/google/gemma-3-4b-it), create a [Hugging Face read token](https://huggingface.co/settings/tokens), and add it to Colab Secrets as `HF_TOKEN`.
6. Set `KB_DIR` to the **same generated TXT folder**. For the example path above, use:

   ```python
   KB_DIR = Path("/content/drive/MyDrive/a-ncsu-courses/DSA495-2026/Data/M08_RAG02/text")
   ```

7. Change the first line of `RAG_PROMPT` to `You are an evidence-based electricity-demand and energy-planning assistant.` and ask questions about the four PDFs. Replace the renewable-energy practice questions in section 8 if you use the optional plots.
8. Run the RAG notebook in order. If you change the knowledge base, rerun document loading, chunking, embeddings, retrieval, and answer generation.

For the **default renewable-energy activity**, use the three original Module 7 TXT files and keep the notebook's default prompt and practice questions. Public source pages are linked below for reference; they are not substitutes for the exact course TXT snapshots.

## Knowledge-source links

- [Columbia / Sabin Center renewable-energy report](https://scholarship.law.columbia.edu/sabin_climate_change/281/)
- [DOE: Frequently Asked Questions about Wind Energy](https://www.energy.gov/cmei/systems/frequently-asked-questions-about-wind-energy)
- [EPA: End-of-Life Solar Panels — Regulations and Management](https://www.epa.gov/hw/end-life-solar-panels-regulations-and-management)

## Course and reading links

- [Course home](https://courseweb.site/dsa495-2026/)
- [Module08 materials and readings](https://courseweb.site/dsa495-2026/materials.html#08)
- [Module07 background materials](https://courseweb.site/dsa495-2026/materials.html#07)
- [Course schedule](https://courseweb.site/dsa495-2026/schedule.html)
- [Lab 2: Semantic Search, RAG, and Evaluation](https://courseweb.site/dsa495-2026/labs.html#lab2)
- [Microsoft Learn: Understand RAG](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/2-understand-rag)
- [Microsoft Learn: Prepare data for retrieval](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/3-prepare-data)
- [Microsoft Learn: Retrieve information and generate a response](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/4-retrieve-generate)
- [Microsoft Learn: Evaluate a RAG solution](https://learn.microsoft.com/en-us/training/modules/rag-fundamentals/5-evaluate-rag)
- [Evidently AI: How to evaluate a RAG system](https://www.youtube.com/watch?v=qI2qQfOG0Js)
- [Sentence Transformers: Retrieve & Re-Rank](https://www.sbert.net/examples/sentence_transformer/applications/retrieve_rerank/README.html)

## Reference tools

- [Gemma 3 model](https://huggingface.co/google/gemma-3-4b-it)
- [MiniLM embedding model](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)
- [Transformers: 4-bit quantization](https://huggingface.co/docs/transformers/v4.57.1/quantization/bitsandbytes)
- [PyMuPDF: text extraction](https://pymupdf.readthedocs.io/en/latest/recipes-text.html)
- [Hands-On Large Language Models: Chapter 8 companion notebook](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models/blob/main/chapter08/Chapter%208%20-%20Semantic%20Search.ipynb)

## Source attribution

The files in `Module08/` are unchanged copies from [SerenaYKim/DSA495-TextAnalysis](https://github.com/SerenaYKim/DSA495-TextAnalysis), imported on October 5, 2026 from commit [18c6786](https://github.com/SerenaYKim/DSA495-TextAnalysis/commit/18c6786334f77f7fe01c539264d04a6d72f2dbae). This top-level README adds navigation and data-connection instructions. No notebook results have been generated in this copy.
