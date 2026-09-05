# DriveQA AI Driving Instructor

> An AI driving assistant that analyses road-scene images, answers driving-safety questions, and explains the reasoning behind its recommendations.

DriveQA AI Driving Instructor is an experimental vision-language project built around the [DriveQA dataset](https://huggingface.co/datasets/DriveQA/DriveQA_Dataset). The notebook prepares driving-intersection examples, fine-tunes and evaluates a Qwen2-VL model, then demonstrates a simple Gradio or Streamlit interface for asking questions about a driving scene.

> **Safety notice:** this project is for research, education, and driving-scenario analysis only. It must not be used as a replacement for a licensed driving instructor, traffic law, or real-time safety-critical driving systems.

## Demo video

Watch or download the project walkthrough: [DriveQA demo video](assets/driveqa-demo.mp4).

## What it can do

- Analyse an image of an intersection or driving scenario.
- Answer questions such as who has priority or what hazards may be present.
- Give an explanation and a concise driving-rule reminder.
- Provide a lightweight Gradio or Streamlit interface after model training.

## Repository contents

| Path | Purpose |
| --- | --- |
| `driveqa-ai-driving-instructor.ipynb` | End-to-end experimentation, data preparation, fine-tuning, evaluation, and UI examples. |
| `assets/driveqa-demo.mp4` | Short project demonstration video. |
| `requirements.txt` | Core Python dependencies used in the notebook. |

## Quick start

1. Create an environment with Python 3.10+ and install PyTorch for your CUDA/CPU setup from [pytorch.org](https://pytorch.org/get-started/locally/).
2. Install the project dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open `driveqa-ai-driving-instructor.ipynb` in Jupyter or Kaggle.
4. Follow the cells to download DriveQA data from Hugging Face, prepare the dataset, and run inference or fine-tuning.

## Model and data

The notebook uses Qwen2-VL for vision-language reasoning and explores BLIP/BLIP-2 baselines. It downloads the DriveQA dataset at runtime; large datasets and trained model checkpoints are intentionally not committed to this repository.

## License and attribution

Please review and respect the licenses and terms for the [DriveQA dataset](https://huggingface.co/datasets/DriveQA/DriveQA_Dataset), Qwen2-VL, and all model dependencies before reuse or redistribution.
