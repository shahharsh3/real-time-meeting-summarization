
Real-Time Meeting Summarization
--------------------------------------------------

This project implements a real-time dialogue summarization system for meeting transcripts using transformer-based models such as BART, 
T5-small, and FLAN-T5-base. It preprocesses multi-speaker dialogues and generates concise, 
abstractive summaries suitable for note-taking and productivity tools.

Project Structure:
- data-preprocessing.ipynb      : Data cleaning, formatting, spell correction
- bart-base-model.ipynb         : Fine-tuning and inference with facebook/bart-base
- t5-small-model.ipynb          : Fine-tuning and inference with t5-small
- flan-t5-base-model.ipynb      : Fine-tuning and inference with google/flan-t5-base
- /data                         : Directory for train/test/validation JSON files
- README.txt                    : This file

Requirements:
- Install standard Python libraries: transformers, datasets, evaluate, nltk, pyspellchecker, pandas

Dataset:
The project uses the SAMSum Corpus, a collection of multi-turn dialogues with human-written summaries. You can load it via Hugging Face or use the provided JSON files in the data/ directory.

How to Run:

1. Data Preprocessing:
   - Run data-preprocessing.ipynb to normalize punctuation, correct spelling, and flatten dialogues.

2. Fine-Tuning Models:
   - Use the corresponding notebook for each model to train and generate summaries:
     - bart-base-model.ipynb
     - t5-small-model.ipynb
     - flan-t5-base-model.ipynb

3. Sample Inference:
   - After training, you can use the pipeline section in each notebook to test summarization with new dialogues. 
	- Use summarization-generator.ipynb to generate summary for all models for comparison

Evaluation:
Model performance is evaluated using ROUGE-1, ROUGE-2, and ROUGE-L metrics. Results and visualizations are embedded in the respective notebooks.

Notes:
- FLAN-T5 generally provides the most faithful and fluent summaries.
- GPU usage is recommended for training.
- This solution can be extended for real-time transcription with additional speech-to-text integration.
