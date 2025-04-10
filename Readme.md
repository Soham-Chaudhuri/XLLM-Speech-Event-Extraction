## WiSE: Speech-to-Structured Events - Shared Task System

This repository contains the full implementation of the system submitted to XLLM Shared Task II (ACL 2025).  
Due to computational constraints, experiments were conducted using free GPU/CPU environments (e.g., Kaggle), and intermediate outputs (e.g., notebook cell outputs) were not preserved.  
However, all model configurations, scripts, and parameters used for training and evaluation are provided and reproducible.

### Structure:
├── dev_transcriptions.csv             # Transcriptions of dev audio (Whisper outputs)
├── test_transcriptions.csv            # Transcriptions of test audio (Whisper outputs)
├── transcriptions - transcriptions.csv# General transcription CSV (possibly train)
├── requirements.txt                   # Python dependencies
├── tokenizer.zip                      # Pretrained tokenizer used for text2event fine-tuning
├── xllm-ner.zip                       # Final model weights and config for text2event+LoRA
│
├── xllm-speech-ner-whisper.ipynb      # Whisper transcription script (ASR stage)
├── xllm-speech-ner-t2e2.ipynb         # Fine-tuning and evaluation of Text2Event2 with LoRA
├── xllm-speech-ner-bert.ipynb         # BERT-NER experiments (not used in final system)
├── xllm-speech-ner-test.ipynb         # Final pipeline used for shared task testing

### Challenges:
   - Dataset provided only audio and event tags, no gold transcripts.
   - Final F1 score ~44 due to hallucinations/noise in Whisper ASR + no gold alignment for training.
   - Training was conducted on CPU due to GPU limitations in free environments.

