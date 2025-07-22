# LLM Digitization and Analysis of Archival Documents

This repository contains code and data for digitizing Latin American guild ordinances and classifying their sentences into economic categories using Large Language Models (LLMs), in particular GPT-4o.

## Getting Started Quickly

This repository is primarily composed of Jupyter notebooks designed for economic historians interested in quantitative analysis of historical guild regulations. You do **not** need strong technical skills to get started.

**Fastest way to get started:**
- Download and install a modern IDE such as [VSCode](https://code.visualstudio.com) or [Cursor](https://cursor.com/en).
- Open the IDE and enter "Agent Mode" (in Cursor, press `Cmd + L`).
- Ask the agent to **clone this repository** and set it up for you. For example, you can write: `Clone https://github.com/niclasgriesshaber/guilds-llm and set it up.`
- The agent will handle the setup, so you can immediately start exploring the notebooks.

You can also explain to the Agent what changes you want to make and put your own data into the project. You can then quickly adjust this repository for your needs.

**Note:** To access GPT-4o for LLM-based analysis, you will need an OpenAI API key. You can generate one at [https://platform.openai.com/api-keys](https://platform.openai.com/api-keys). The API key must be inserted in one of the code cells (prior to any LLM API calls) in the Jupyter notebooks. All relevant cells are clearly commented to guide you through this process. Alternatively, you can also create an .env file to store your API keys there.

## Repository Structure (Refined)

- **01_llm_digitization/**
  - **llm_digitization_code/**
    - `01_llm_digitization_pipeline.ipynb`: Main notebook for digitizing archival image scans of guild ordinances.
    - `02_text_files_to_csv.ipynb`: Converts text files of guild ordinances into structured CSV datasets.
  - **llm_digitization_data/**
    - **archival_image_scans/**: Contains subfolders with original image scans (TIFF format) of guild ordinances from Mexico and Peru. *Note: These files are not tracked in git and are available upon request for replication.*
    - **full_text_data/**: Contains plain text transcriptions of the full content of each ordinance, organized by country and guild.
    - **regulations_text_data/**: Contains only the regulatory paragraphs from each ordinance, as plain text files, organized by country and guild.

- **02_llm_classification/**
  - `llm_classification.ipynb`: Notebook for classifying sentences from the ordinances into economic categories using GPT-4o.

- **03_probit_regression/**
  - `01_transform_dataset.ipynb`: Transforms LLM classification results into a sentence-level dataset for analysis.
  - `02_probit_regression.ipynb`: Performs probit regression analysis on the sentence-level dataset.
  - `probit_regression_results.txt`: Contains the results and average marginal effects from the regression analysis.

- **datasets/**
  - `llm_classification_results.csv`: Results of the LLM-based classification.
  - `regulations_dataset.csv`: Structured dataset of guild regulations.
  - `sentence_dataset.csv`: Sentence-level dataset derived from classification results.
  - **summary_statistics/**
    - `summary_statistics.ipynb`: Notebook for generating and exploring summary statistics of the datasets.

- **environment.yaml**: Environment specification file for easy setup of dependencies (can be used with `conda` or similar tools).
- **README.md**: This file, providing an overview and instructions.

## Acknowledgements

We would like to thank Jeremy Edwards, Mattia Fochesato, Jane Humphries, Joel Mokyr, and Andreas Schanbacher for their valuable comments and suggestions; participants at the Annual Graduate Workshops at All Souls College, University of Oxford, in 2023 and 2024, for their stimulating feedback; and the Economic and Social History Master's Programme at the University of Oxford (2022–2023) for awarding the Joan Thirsk Dissertation Prize to Niclas Griesshaber. This repository and the associated paper are based on research conducted as part of that master's thesis.

## Citation

*Please cite this repository and related publications as appropriate. A formal citation will be provided here soon.*