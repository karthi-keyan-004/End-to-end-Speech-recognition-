# End-to-end-Speech-recognition-
Using RNN 
Hybrid HMM-RNN Speech-to-Text Pipeline
This project is a complete and modular Hybrid HMM-RNN Speech-to-Text Pipeline that uses:

Librosa for audio preprocessing and MFCC extraction.
PyTorch for training an RNN acoustic model and a Seq2Seq decoder.
KenLM (optional) for language model-based beam search decoding.
LJSpeech Dataset for training and evaluation.
Features
Preprocessing: VAD, noise reduction, normalization, MFCC extraction.
Training: Acoustic model (LSTM), Seq2Seq decoder.
Evaluation: Word Error Rate (WER) computation.
Inference: Predict transcription for a given audio file.
Optional: Language Model based decoding with KenLM.
Files
main.py: End-to-end training and inference pipeline.
dataset/: Folder containing LJSpeech dataset with wavs/ and metadata.csv.
How to Use
Prepare Dataset: Download LJSpeech-1.1 and extract it to /content/dataset/LJSpeech-1.1/.

Run the Script:

python main.py
Inference:

hypothesis = inference("path/to/audio.wav", input_dim=13, hidden_dim=128, output_dim=256, use_kenlm=False)
print(hypothesis)
Requirements
torch
numpy
librosa
tqdm
kenlm (optional)
Acknowledgements
LJSpeech Dataset
Librosa
KenLM
