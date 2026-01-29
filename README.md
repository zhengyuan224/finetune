# LLM Finetuning Project

This repository contains scripts, notebooks, and configuration files for finetuning Large Language Models (LLMs), specifically focused on Qwen and Llama3 architectures using LoRA (Low-Rank Adaptation).

## Project Structure

```text
.
├── configs/            # YAML configuration files for training and inference
│   ├── llama3_lora_sft.yaml
│   └── infer.yaml
├── data/               # Datasets for training and testing
│   ├── data.json
│   ├── round1_train_data.jsonl
│   └── round1_test_data.jsonl
├── notebooks/          # Jupyter notebooks for experimentation and data processing
│   ├── modelscope.ipynb
│   ├── output.ipynb
│   └── Untitled*.ipynb
└── README.md
```

## Quick Start

### 1. Environment Setup
Ensure you have the necessary dependencies installed (e.g., `llama-factory`, `modelscope`).

### 2. Data Preparation
Place your training and test data in the `data/` directory. Currently, the project uses `.json` and `.jsonl` formats.

### 3. Training
Use the configurations in `configs/` to start the finetuning process. For example, using LLaMA-Factory:
```bash
llamafactory-cli train configs/llama3_lora_sft.yaml
```

### 4. Inference
Check `notebooks/` for inference examples or use the `configs/infer.yaml` with the appropriate inference script.

## Notes
- The default model path is set to `/root/autodl-tmp/qwen/Qwen2-7B-Instruct`. Please update this in the config files if your model is located elsewhere.
- The training uses LoRA SFT (Supervised Fine-Tuning).
