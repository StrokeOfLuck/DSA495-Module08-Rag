# Course data

The four Module08 PDFs supplied by Sean on October 5, 2026 are included unchanged in [M08_RAG02/](M08_RAG02/). Matching extracted text is in [M08_RAG02/text/](M08_RAG02/text/).

| PDF | Pages | Extracted words | TXT |
| --- | ---: | ---: | --- |
| [D00000-ElectricVehicleScenarioAnalysisWorkshopSeries.pdf](M08_RAG02/D00000-ElectricVehicleScenarioAnalysisWorkshopSeries.pdf) | 15 | 5,199 | [Text](M08_RAG02/text/D00000-ElectricVehicleScenarioAnalysisWorkshopSeries.txt) |
| [D00001-TheEraOfFlatPowerDemandIsOver.pdf](M08_RAG02/D00001-TheEraOfFlatPowerDemandIsOver.pdf) | 29 | 6,083 | [Text](M08_RAG02/text/D00001-TheEraOfFlatPowerDemandIsOver.txt) |
| [D00002-CharacteristicsAndRiskOfEmergingLargeLoads(1).pdf](M08_RAG02/D00002-CharacteristicsAndRiskOfEmergingLargeLoads%281%29.pdf) | 49 | 18,336 | [Text](M08_RAG02/text/D00002-CharacteristicsAndRiskOfEmergingLargeLoads%281%29.txt) |
| [D00003-PlanningForAndManagingInterminateElecricLoads.pdf](M08_RAG02/D00003-PlanningForAndManagingInterminateElecricLoads.pdf) | 20 | 5,828 | [Text](M08_RAG02/text/D00003-PlanningForAndManagingInterminateElecricLoads.txt) |

The PDF notebook downloads the PDFs from GitHub and performs extraction. The RAG notebook defaults to the four committed TXT files, so it works in a separate Colab runtime without mounting Drive or copying outputs.

Text was extracted with PyMuPDF using sorted text blocks, whitespace normalization, blank lines between blocks, and form-feed separators between pages, matching the PDF notebook. Tables, charts, and reading order should still be checked against the PDFs. See [manifest.json](manifest.json) for source hashes and extraction metadata.

[Original Module08 course data folder](https://drive.google.com/drive/folders/1e5EMCMr8OK7kCsNo6-J02EI1rpdZfxKZ), linked from the [course schedule](https://courseweb.site/dsa495-2026/schedule.html).

## Optional Module7 collection

The three original Module7 Columbia / DOE / EPA TXT files are not included. They can be added to `data/M07_RAG01/` to enable `KB_COLLECTION = "M07_RAG01"`. [Original course folder](https://drive.google.com/drive/folders/1xcAec1cOwCR-eBxsSlm_RVS46zjgowS1). Module7 data is not required for the default Module08 workflow.

Model weights download from Hugging Face separately and are not repository data.
