# DSA 495 — Module 08: RAG II

Sean Ryan's copy of the [Module08 course materials](https://github.com/SerenaYKim/DSA495-TextAnalysis/tree/master/Module08), taught by Serena Kim at NC State.

## Open the notebooks

| Notebook | View on GitHub | Run in Google Colab | Runtime |
| --- | --- | --- | --- |
| Convert PDFs to text | [PDF-to-Text](Module08/DSA495-M08-PDF-to-Text.ipynb) | [Open in Colab](https://colab.research.google.com/github/StrokeOfLuck/DSA495-Module08-Rag/blob/main/Module08/DSA495-M08-PDF-to-Text.ipynb) | CPU |
| Retrieve evidence and generate cited answers | [RAG with Gemma 3](Module08/DSA495-M08-RAG-Gemma3.ipynb) | [Open in Colab](https://colab.research.google.com/github/StrokeOfLuck/DSA495-Module08-Rag/blob/main/Module08/DSA495-M08-RAG-Gemma3.ipynb) | T4 GPU |

[Original Module08 instructions](Module08/README.md)

## Data loads directly from GitHub

Both notebooks now download their inputs from this repository. The instructor's personal Google Drive paths and Drive-mount cells have been removed.

**Module08 data is included:** all four supplied PDFs and their extracted TXT files are committed in this repo. Both notebooks download what they need automatically. The optional Module7 TXT collection is not included.

| Collection | Repository destination | Source folder |
| --- | --- | --- |
| Four supplied Module08 PDFs (`D00000`–`D00003`) | [data/M08_RAG02/](data/M08_RAG02/) | [Course Module08 PDFs](https://drive.google.com/drive/folders/1e5EMCMr8OK7kCsNo6-J02EI1rpdZfxKZ) |
| Three Module7 renewable-energy TXT files | [data/M07_RAG01/](data/M07_RAG01/) | [Course Module7 TXT files](https://drive.google.com/drive/folders/1xcAec1cOwCR-eBxsSlm_RVS46zjgowS1) |

To run the Module08 workflow:

1. Open **PDF-to-Text** in Colab with a CPU runtime and run it in order. It downloads the four PDFs from GitHub and generates TXT files.
2. Open **RAG with Gemma 3** with a T4 GPU. Its default `KB_COLLECTION = "M08_RAG02"` downloads the four matching TXT files directly from GitHub, including in a separate runtime.
3. Accept [Gemma's terms](https://huggingface.co/google/gemma-3-4b-it) and put a [Hugging Face read token](https://huggingface.co/settings/tokens) in Colab Secrets as `HF_TOKEN`.
4. To run the optional original Module7 activity, first add its three original TXT files, then set `KB_COLLECTION = "M07_RAG01"`. It downloads the three TXT files from GitHub.

[Data status and upload locations](data/README.md). The notebooks check for the required files and stop with a clear error if they are missing. Model weights are loaded only after the RAG data check.

If you already have a notebook open in Colab, reopen it using the links above to load the updated version.

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

The notebooks in `Module08/` were adapted from [SerenaYKim/DSA495-TextAnalysis](https://github.com/SerenaYKim/DSA495-TextAnalysis), imported on October 5, 2026 from commit [18c6786](https://github.com/SerenaYKim/DSA495-TextAnalysis/commit/18c6786334f77f7fe01c539264d04a6d72f2dbae). The adaptations replace Drive-dependent loading with GitHub downloads, default the RAG notebook to the Module08 PDF collection, and check inputs before model loading. The four PDFs were supplied by Sean; their TXT files were generated with the notebook's extraction method. This top-level README adds navigation and source links. No RAG answers have been generated in this copy.
