# Agricultural Land Classification with CNN and Vision Transformer Models

This project focuses on building and comparing deep learning models for agricultural land classification. It uses image datasets to distinguish between agricultural and non-agricultural land, and evaluates multiple model architectures including convolutional neural networks (CNNs) and vision transformers (ViTs).

The repository brings together data preparation, model training, evaluation, and comparative analysis in a structured workflow, making it suitable for experimentation and repeatable benchmarking.

## Project Overview

The main objective is to classify land-use imagery into meaningful categories using modern computer vision approaches. The project includes:

- data loading and preprocessing workflows
- image augmentation strategies
- CNN-based classifier implementation
- Vision Transformer-based classifier implementation
- side-by-side comparison between Keras and PyTorch implementations
- model evaluation using standard metrics and visual analysis

## Key Features

- Multi-architecture experimentation with CNN and ViT pipelines
- Training and evaluation notebooks for Keras and PyTorch
- Support for structured model comparison and reporting
- Local artifact management for model checkpoints and logs
- Flexible configuration for project settings and runtime parameters

## Repository Structure

```text
.
├── .gitignore                 # git ignore rules
├── README.md                  # project documentation
├── config/
│   ├── __pycache__/
│   ├── config.yaml
│   └── config_loader.py
├── environment.yml            # Conda environment setup
├── logs/
│   └── agent.log
├── main.py                    # project entry point
├── models/
│   ├── .DS_Store
│   ├── 1-Data-Loading/
│   │   └── memort-vs-generator-data-loading.ipynb
│   ├── 2-Data-Loading-And-Augmentation/
│   │   └── .DS_Store
│   ├── 3-Convolutional-Neural-Networks/
│   │   └── .DS_Store
│   └── 4-CNN-Vision-Transformer-Integration/
│       └── .DS_Store
├── requirements.txt           # Python dependencies
├── sample-notebook/
│   └── memory-vs-generator-based-data-loading.ipynb
├── services/
│   ├── __init__.py
│   └── translator.py
├── setup.py
├── tests/
│   ├── __init__.py
│   └── test_agent.py
├── utils/
│   ├── __init__.py
│   └── helpers.py
└── venv/
    ├── .DS_Store
    ├── bin/
    ├── lib/
    └── pyvenv.cfg
```

## Technology Stack

The project uses a deep learning stack centered on Python, PyTorch, TensorFlow/Keras, scikit-learn, and supporting data science libraries. The dependencies include:

- PyTorch
- TensorFlow / Keras ecosystem
- Transformers
- scikit-learn
- NumPy and Pandas
- Matplotlib and Plotly
- OpenAI and other LLM-related packages for experimentation
- LangChain and vector-store integrations
- Datasets and sentence-transformers tools

## Environment Setup

### Option 1: Conda

```bash
conda env create -f environment.yml
conda activate llms
```

### Option 2: Python virtual environment

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Data Requirements

The project expects a local dataset directory that is not committed to source control.

Recommended location:

```text
data/images_dataSAT/
```

The repository is configured to ignore the data directory so large files are not pushed to Git. Download or mount the dataset locally before running the notebooks.

## Running the Project

### Python entry point

```bash
python main.py
```

### Notebook workflow

Open the notebooks in the model folders under `models/` to explore:

- data loading and augmentation
- CNN training and evaluation
- ViT training and evaluation
- keras vs pytorch comparison

## Model and Experiment Organization

The `models/` directory contains experiment tracks organized by topic and framework. Notable folders include:

- `models/1-Data-Loading/`
- `models/2-Data-Loading-And-Augmentation/`
- `models/3-Convolutional-Neural-Networks/`
- `models/4-CNN-Vision-Transformer-Integration/`

These folders contain notebook-based experiments and saved model artifacts for local comparison.

## Logging and Output Artifacts

Training runs, checkpoints, and logs are stored locally in the `logs/` directory and model folders. These artifacts are intentionally excluded from Git so that generated outputs and large model files do not clutter the repository.

## Configuration

Project configuration is kept in the `config/` folder and should remain local to the workspace. Anything sensitive should be stored outside version control using environment-based settings.

## Security Notes

This repository does not include any checked-in API key material. Local environment files, secrets, and generated artifacts are excluded through `.gitignore` to reduce the risk of accidentally committing sensitive data.

## Project Status

This workspace is structured as a research and experimentation project for image classification using CNN and Vision Transformer architectures. It is intended for local development, experimentation, and model analysis rather than deployment.

## Author

- Author: Abhishek Singh
- Email: abhikusi73@gmail.com
