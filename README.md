# 🌲 ML Assignment 3 — Machine Learning Pipeline

[![Python Version](https://img.shields.io/badge/python-3.10-blue)](https://www.python.org/)

---

## 📖 Table of Contents

1. [Project Overview](#project-overview)
2. [Project Structure](#project-structure)
3. [Setup Instructions](#setup-instructions)
4. [Running the Pipeline](#running-the-pipeline)
5. [Outputs](#outputs)
6. [Logging](#logging)
7. [Troubleshooting](#troubleshooting)
8. [Notes](#notes)

---

## 🏗️ Project Overview

This repository implements a **complete machine learning pipeline** for predicting **forest cover types** using cartographic variables.  
The pipeline automates the following tasks:

- Data ingestion  
- Validation  
- Transformation  
- Model training  
- Evaluation  

All stages are controlled via **YAML configuration files**, providing flexibility to update paths, parameters, or schema **without modifying code**.

---

## 📂 Project Structure

### Root Files
| File | Description |
|------|------------|
| `main.py` | Executes the full end-to-end pipeline sequentially |
| `params.yaml` | Stores model hyperparameters |
| `config.yaml` | Manages file paths and component settings |
| `schema.yaml` | Defines input dataset structure for validation |
| `requirements.txt` | Lists Python dependencies |
| `README.md` | Project overview and instructions |

---

### src/ — Main Project Modules
| Folder / File | Description |
|---------------|------------|
| `components/` | Individual pipeline stages (ingestion, validation, transformation, training, evaluation) |
| `config/` | Loads YAML settings dynamically via configuration manager |
| `constants/` | Global constants (paths, schema references, etc.) |
| `entity/` | Data classes for configuration and artifacts |
| `pipeline/` | Scripts to run each pipeline stage independently |
| `utils/` | Helper functions for saving models, reading YAMLs, etc. |

---

### artifacts/ — Runtime Outputs

Automatically created when `main.py` is executed. Contains:

- Processed datasets (`train.csv`, `test.csv`)  
- Trained model (`model.joblib`)  
- Evaluation results (`metrics.json`)  
- Logs and status reports  

---

### research/

Contains **experimental Jupyter notebooks** to test data loading, transformations, and model behavior before integrating into the pipeline.

---

### logs/

Structured runtime logs for **debugging and auditing**.
logs/
├── running_log.log # standard runtime logs
└── error_log.log # detailed error logs (if any)

