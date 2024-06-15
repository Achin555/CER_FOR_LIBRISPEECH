# CER_FOR_LIBRISPEECH

Speech Transcription and Evaluation with Whisper and LibriSpeech Dataset
Overview:
This Python script demonstrates the transcription of audio data using the Whisper model and evaluates the transcription quality using the Character Error Rate (CER) metric. It utilizes the LibriSpeech dataset for training and evaluation, focusing on a small subset for demonstration purposes.

Setup:
Ensure the following packages are installed:

bash
Copy code
pip install datasets transformers openai-whisper jiwer soundfile librosa evaluate
These packages are necessary for handling datasets (datasets), loading models (transformers, openai-whisper), computing metrics (jiwer, evaluate), and handling audio data (soundfile, librosa).

Usage:
Dataset Loading: The script loads a subset of the LibriSpeech dataset using load_dataset, ensuring trust in remote code execution.

Model Loading: Utilizes the pre-trained Whisper model (whisper.load_model("base")) for transcribing audio.

Transcription Function: Defines transcribe(batch) to process audio batches, converting and transcribing 16kHz audio data to text.

Evaluation: Computes the Character Error Rate (CER) metric using evaluate.load("cer", trust_remote_code=True), evaluating the accuracy of transcriptions against reference texts.

Output: Prints the computed CER to evaluate the transcription quality (print(f"CER: {cer:.4f}")).

Benefits:
This script showcases the integration of state-of-the-art AI models (Whisper) and robust evaluation metrics (CER) for speech transcription tasks. It provides a foundational example for researchers and developers interested in automated speech recognition (ASR) and natural language processing (NLP) applications.

Limitations:
Ensure adequate system resources for handling large datasets and model computations. Adjustments may be necessary for scaling to larger datasets or deploying in production environments.
