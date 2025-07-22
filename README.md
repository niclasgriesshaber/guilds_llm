# LLM Digitization and Analysis of Archival Documents

This repository contains code and data for digitizing Latin American guild ordinances and classifying their sentences into economic categories using Large Language Models (LLMs).

## Repository Structure

- **01_llm_digitization/**
  - **llm_digitization_code/**
    - `01_llm_digitization_pipeline.ipynb`: Digitizes archival image scans displaying guild ordinances.
    - `02_text_files_to_csv.ipynb`: Converts guild ordinance text files to `regulations_dataset.csv`.
  - **llm_digitization_data/**
    - **archival_image_scans/**: Image scans from Mexican and Peruvian guild ordinances.
    - **full_text_data/**: Digitized text data from image scans.
    - **regulations_text_data/**: Digitized text data from image scans. Regulation paragraphs only.

- **02_llm_classification/**
  - `llm_classification.ipynb`: Classifies digitized guild ordinance sentences using GPT-4.

- **03_probit_regression/**
  - `01_transform_dataset.ipynb`: Transforms `llm_classification_results.csv` into `sentence_dataset.csv`
  - `02_probit_regression.ipynb`: Performs probit regression analysis on `sentence_dataset.csv`
  - `probit_regression_results.txt`: Probit regression results with average marginal effects.

- **datasets/**
  - `llm_classification_results.csv`: LLM-based classification results.
  - `regulations_dataset.csv`: Dataset containing guild regulations.
  - `sentence_dataset.csv`: Sentence-level dataset based on `llm_classification_results.csv`.
  - **summary_statistics/**
    - `summary_statistics.ipynb`

## Acknowledgements

We would like to thank Jeremy Edwards, Mattia Fochesato, Jane Humphries, Joel Mokyr, and Andreas Schanbacher for their valuable comments and suggestions; participants at the Annual Graduate Workshops at All Souls College, University of Oxford, in 2023 and 2024, for their stimulating feedback; and the Economic and Social History Master's Programme at the University of Oxford (2022–2023) for awarding the Joan Thirsk Dissertation Prize to Niclas Griesshaber. This repository and the associated paper are based on research conducted as part of that master's thesis.

## Citation

*Please cite this repository and related publications as appropriate. A formal citation will be provided here soon.*