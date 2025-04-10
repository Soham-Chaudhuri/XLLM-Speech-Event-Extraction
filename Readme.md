## WiSE: Speech-to-Structured Events - Shared Task System

This repository contains the full implementation of the system submitted to XLLM Shared Task II (ACL 2025).  
Due to computational constraints, experiments were conducted using free GPU/CPU environments (e.g., Kaggle), and intermediate outputs (e.g., notebook cell outputs) were not preserved.  
However, all model configurations, scripts, and parameters used for training and evaluation are provided and reproducible.

### Structure:
- `/whisper_transcribe/` - Scripts for converting audio to transcript using Whisper-medium
- `/event_extraction/` - Fine-tuning Text2Event2 using LoRA
- `/bert_ner/` - Experiments with BERT-based NER (not used in final system)
- `train.py` - Final pipeline used for shared task
- `config.json` - LoRA + training parameters
- `evaluation.py` - Scoring script
