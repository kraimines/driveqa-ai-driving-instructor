# DriveQA AI Driving Instructor

An AI-powered driving assistant that analyzes road-scene images, answers driving-safety questions, and explains the reasoning behind its recommendations.

## Overview

DriveQA AI Driving Instructor is an experimental vision-language project built around the [DriveQA Dataset](https://huggingface.co/datasets/DriveQA/DriveQA_Dataset).

The project explores how multimodal large language models (VLMs) can be adapted to understand driving scenes and provide natural-language answers to questions about road situations.

The main workflow includes:

- Preparing and processing driving-intersection examples from the DriveQA dataset.
- Fine-tuning a Qwen2-VL vision-language model on driving-related question-answer pairs.
- Evaluating the model on driving-scenario questions.
- Demonstrating the model through an interactive Gradio / Streamlit interface.
- Generating explanations that describe why a particular driving action is recommended.

The goal is to investigate whether vision-language models can combine visual understanding, driving knowledge, and natural-language reasoning in a single system.

## Features

- 🖼️ **Road-scene understanding** — analyze images containing intersections and other driving situations.
- 💬 **Driving Q&A** — ask questions about what is happening in a scene.
- 🧠 **Reasoning explanations** — provide an explanation for the recommended action.
- 🤖 **Vision-language model** — built around Qwen2-VL.
- 📚 **DriveQA dataset** — uses real-world driving-question-answer examples.
- 🏋️ **Model fine-tuning** — adapts a pretrained VLM to the driving domain.
- 📊 **Model evaluation** — evaluate responses on driving scenarios.
- 🌐 **Interactive demo** — experiment with the trained model through a Gradio or Streamlit interface.

## Project Pipeline

```text
                 DriveQA Dataset
                       │
                       ▼
              Data Preparation
                       │
                       ▼
          Driving Scene / QA Examples
                       │
                       ▼
              Qwen2-VL Fine-tuning
                       │
                       ▼
                 Model Evaluation
                       │
                       ▼
             Interactive Application
                ┌──────┴──────┐
                ▼             ▼
             Gradio       Streamlit
                │             │
                └──────┬──────┘
                       ▼
              Driving Scene Q&A
```

## Model

The project uses Qwen2-VL, a multimodal vision-language model capable of processing both images and text.

The model is adapted to the driving domain using examples from DriveQA. Given a road-scene image and a question, the model produces a natural-language response describing the appropriate driving decision.

For example:

**Input:**

`[Road-scene image]`

**Question:**

> What should the driver do at this intersection?

**Model:**

> The driver should slow down and yield to the approaching vehicle because the other vehicle has priority at the intersection.

The exact behavior and quality of the responses depend on the dataset, preprocessing, training configuration, and model checkpoint used.

## Installation

### Prerequisites

- Python 3.10 or later
- Git
- A CUDA-compatible GPU is recommended for fine-tuning and inference with Qwen2-VL

### 1. Clone the repository

```bash
git clone https://github.com/kraimines/driveqa-ai-driving-instructor.git
cd driveqa-ai-driving-instructor
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install PyTorch and the project dependencies

Install the PyTorch build appropriate for your CPU or CUDA version by following the [official PyTorch installation guide](https://pytorch.org/get-started/locally/), then run:

```bash
pip install -r requirements.txt
```

### 4. Run the project

Open `driveqa-ai-driving-instructor.ipynb` in Jupyter Notebook, JupyterLab, or Kaggle and run the cells in order. The notebook downloads the DriveQA dataset, prepares the data, and includes examples for training, evaluation, and launching a Gradio or Streamlit demo.

## Demo video

Watch or download the project walkthrough: [DriveQA demo video](assets/driveqa-demo.mp4).
