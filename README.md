# LLM Fine-Tuning Project

This project contains code and configuration files for fine-tuning a Large Language Model (LLM) using PEFT (Parameter-Efficient Fine-Tuning) techniques.

## 📁 Project Structure

```
llm-finetuning/
├── data/                    # Training and evaluation datasets
├── model/                   # Base model and fine‑tuned model storage
├── scripts/                 # Training, evaluation, and utility scripts
├── configs/                 # Adapter and training configuration files
├── adapter_config.json      # PEFT adapter configuration
├── adapter_model.bin        # Trained adapter weights
├── train.py                 # Script for fine‑tuning
├── evaluate_model.py        # Script for evaluation
└── README.md                # Documentation
```

## 🚀 Features

* Fine‑tuning using PEFT (LoRA/Adapter-based approach)
* Evaluation script for checking model performance
* Config files for easy reproducibility
* Supports HuggingFace models and datasets

## 🔧 Requirements

Install all dependencies:

```
pip install -r requirements.txt
```

## 🏋️‍♂️ Training

Run the training script:

```
python train.py
```

You can modify parameters in `configs/` as needed.

## 📈 Evaluation

```
python evaluate_model.py
```

This loads the fine‑tuned adapter (`adapter_model.bin`) and evaluates the model.

## 🧩 Common Issue

**Error: adapter_model.bin paste nahi ho raha / load nahi ho raha?**

* Ensure the path in your script matches the location of `adapter_model.bin`
* The directory must contain BOTH `adapter_config.json` and `adapter_model.bin`
* Example:

```
model = PeftModel.from_pretrained(base_model, "./model/adapters/")
```

## 📜 License

This project is for educational and experimental use.

## 🙌 Author

Shubham – Fine‑tuning LLM experiments.
