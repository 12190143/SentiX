# SentiX
This is the source code of our COLING 2020 paper <SentiX: A Sentiment-Aware Pre-Trained Model for Cross-domain Sentiment Analysis>


## Requirements

* Python 3.6 or higher.
* [PyTorch](http://pytorch.org/) 1.2.0.
* [transformers](https://github.com/huggingface/transformers) PyTorch 1.2.0.

## Pre-trained Models (PyTorch)
The following pre-trained models are available for download from Google Drive:
* [`SentiX`](https://drive.google.com/file/d/1aURbb0d5n-eFn2QxAWX64gA8X7b9xC2n/view?usp=sharing): 
PyTorch version, same setting with BERT-base，loading model with transformers.

## Training

To train SentiX, simply run:
```
python pretrain_multigpu_final.py --dataset data_all --max_seq_len 256 --batch_size 16 --gradient_accumulation_steps 4 
```
## Evaluation Instructions

To test after setting model path:
```
run_multidomain_sentiment_analysis.sh
```

## File Structure
- pretrain_multigpu_final.py: main file of pre-trained model
- data_processing: data processing
- models： our models
- data_utils_pretrain_final.py: data_loader


