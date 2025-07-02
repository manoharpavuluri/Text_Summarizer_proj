# Text Summarizer Project

## Overview
Text Summarizer is a Python-based NLP application designed to generate concise and meaningful summaries from large bodies of text. Leveraging state-of-the-art transformer models, this project provides a modular, extensible framework for text summarization tasks, suitable for research, prototyping, and production deployment.

## Features
- **Abstractive and Extractive Summarization** using HuggingFace Transformers
- **Configurable Pipelines** for easy experimentation
- **Custom Logging** for traceability
- **YAML-based Configuration** for reproducibility
- **Jupyter Notebook Support** for research and prototyping
- **Docker Support** for containerized deployment
- **FastAPI Integration** for serving models as APIs

## Tech Stack
- Python 3.7+
- HuggingFace Transformers
- Datasets, NLTK, Pandas
- PyTorch
- FastAPI & Uvicorn
- PyYAML, Box, Ensure
- Jinja2 (for templating)
- Docker

## Project Structure
```
Text_Summarizer_proj/
├── app.py                # (Entry point for API, currently a placeholder)
├── main.py               # (Logger test entry point)
├── config/
│   └── config.yaml       # (Project configuration)
├── params.yaml           # (Model/experiment parameters)
├── src/
│   └── textSummarizer/
│       ├── components/   # (Summarization components)
│       ├── config/       # (Configuration management)
│       ├── constants/    # (Constant values)
│       ├── entity/       # (Entity definitions)
│       ├── logging/      # (Custom logger setup)
│       ├── pipeline/     # (Pipeline orchestration)
│       ├── utils/        # (Utility functions)
│       └── conponents/   # (Typo, should be merged with components)
├── requirements.txt      # (Python dependencies)
├── Dockerfile            # (Containerization)
├── setup.py              # (Packaging)
├── research/
│   └── trials.ipynb      # (Experiment notebook)
└── README.md             # (Project documentation)
```

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/manoharpavuluri/Text_Summarizer_proj.git
   cd Text_Summarizer_proj
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **(Optional) Run in Docker:**
   ```bash
   docker build -t text-summarizer .
   docker run -p 8000:8000 text-summarizer
   ```

## Usage
- **Run logger test:**
  ```bash
  python main.py
  ```
- **(Planned) Run API server:**
  ```bash
  uvicorn app:app --reload
  ```
- **Experiment in Jupyter:**
  Open `research/trials.ipynb` in Jupyter Notebook.

## Configuration
- **config/config.yaml**: Main configuration file (currently empty, to be populated as needed).
- **params.yaml**: Model and experiment parameters (currently empty).

## Key Modules
- `src/textSummarizer/utils/common.py`: Utility functions for YAML reading, directory creation, and file size calculation.
- `src/textSummarizer/logging/__init__.py`: Custom logger setup for consistent logging across modules.

## Dependencies
See `requirements.txt` for the full list. Key packages:
- `transformers`, `datasets`, `torch`, `nltk`, `pandas`, `fastapi`, `uvicorn`, `PyYAML`, `python-box`, `ensure`, `Jinja2`, `matplotlib`, `boto3`, `mypy-boto3-s3`, `notebook`

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Future Improvements
- Implement actual summarization pipelines and models
- Populate and document `config.yaml` and `params.yaml`
- Merge/remove the typo directory `conponents/`
- Add unit and integration tests
- Expand API endpoints and add authentication
- Add support for more summarization models
- Improve error handling and logging
- Add CI/CD workflows and deployment scripts
- Enhance documentation with usage examples and API docs

## Contributing
Contributions are welcome! Please open issues or pull requests for suggestions and improvements.