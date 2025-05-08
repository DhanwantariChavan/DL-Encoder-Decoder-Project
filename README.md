📰 Headline Generator using Encoder-Decoder and Transformer Models
A Comparative Study of LSTM Models Without Attention, With Attention, and Transformers for News Headline Generation
This project explores automated news headline generation using three deep learning architectures:

Basic LSTM Encoder-Decoder (without attention)

LSTM Encoder-Decoder with Attention

Transformer Model (Self-Attention)

We evaluate and compare performance using BLEU and ROUGE metrics, aiming to understand how attention mechanisms and self-attention impact summarization quality.

🔍 Project Overview
🔧 Architectures Implemented:
LSTM Encoder-Decoder (No Attention):
Simple sequence-to-sequence model with greedy decoding.

LSTM with Attention:
Uses a bidirectional encoder and additive attention mechanism. Helps the decoder focus on relevant parts of the input sequence.

Transformer:
Implements self-attention, positional encoding, and parallelized computation as per “Attention Is All You Need”.

📂 Dataset & Preprocessing
Input: CSV file with text (news articles) and headlines.

Preprocessing Steps:

Lowercasing, punctuation removal, tokenization (NLTK)

Vocabulary built from tokens with frequency ≥ 2

Special tokens: <pad>, <sos>, <eos>, <unk>

Padding: Articles → 400 tokens, Headlines → 20 tokens

Dataset Split: 80% Train, 10% Validation, 10% Test

📊 Evaluation Metrics
BLEU (1–4)

ROUGE (ROUGE-1, ROUGE-2, ROUGE-L)

These metrics are calculated across all three models for fair comparison.

📈 Key Results
Model	BLEU-4	ROUGE-L	Inference Time
LSTM (No Attention)	✅ Basic	✅ Baseline	🕒 Slow
LSTM + Attention	🔼 Better context	🔼 Higher fluency	⚡ Faster
Transformer	⭐ Highest	⭐ Best coherence	⚡⚡ Fastest

Actual metric values are displayed in the notebook.

📌 Key Findings
Attention significantly improves coherence and relevance.

Transformers outperform LSTM-based models in both speed and quality.

Attention maps offer interpretable predictions.

Cleaned data and curated vocabulary boost accuracy.

🛠 Libraries & Tools Used
Python, PyTorch, NLTK, Matplotlib

BLEU/ROUGE metrics
