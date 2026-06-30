# Fine-Tuning Qwen2.5-1.5B-Instruct on OpenHermes
## Overview 
This project fine-tunes Qwen2.5-1.5B-Instruct on the OpenHermes-2.5 instruction dataset using a custom PyTorch training loop. Training utilises PagedAdamW8bit for efficient memory optimisation, with model evaluation based on perplexity and ROUGUE, calculated with prompt tokens masked so only the responses are scored. 

## Project Structure
```
├── data.ipynb  # Data loading, tokenisation, training, and evaluation
└── README.md
```
## Dependencies 
All required packages are installed using "!pip install" commands. 
No separate requirements.txt is needed.

## How to Run
This project was developed in Google Colab with checkpoints saved to Google Drive. To reproduce results:
1. Mount Google Drive as prompted in Colab
2. Run 'data.ipynb' in full to load data, tokenise, and begin training
3. Trained model weights are saved and reloaded for inference and evaluation
A Google account and GPU runtime are required.

## Data Sources
* Base model: Qwen2.5-1.5B-Instruct (Qwen) - https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct
* Training data: OpenHermes-2.5 (teknium) - https://huggingface.co/datasets/teknium/OpenHermes-2.5
