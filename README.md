# VoxStrata

A data-centric pipeline for speech recognition refinement, error analysis, and robust evaluation.

## Overview

VoxStrata provides an end-to-end framework for improving Automatic Speech Recognition (ASR) systems through:

- Model fine-tuning (Whisper)
- Transcript cleanup and normalization
- Error analysis and correction
- Lattice-based evaluation for fair WER computation

The project focuses on handling real-world conversational speech where multiple valid transcriptions exist.


## Features

- Fine-tuning pipeline for Whisper models  
- Number normalization (Hindi spoken → numeric form)  
- English word detection in multilingual transcripts  
- Word-level error classification with confidence scoring  
- Lattice-based WER for fair ASR evaluation  
- Optimized inference via CTranslate2  


## Inference Optimization
```bash 
ct2-transformers-converter \
  --model ./whisper-hi-finetuned \
  --output_dir ./whisper-hi-ct2 \
  --copy_files tokenizer.json preprocessor_config.json \
  --quantization float16
```