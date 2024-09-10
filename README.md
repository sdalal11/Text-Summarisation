# Text-Summarization-with-Seq2Seq

## What is Text Summarization?

Text summarization is the task of using an algorithm to convert long prose text into short, concise, and comprehensive summaries. These summaries preserve the key meaning and context of the original text while remaining sequential and easy to follow.

## Why is it Important?

- Reduces the time spent skimming through lengthy documents, articles, and blogs.
- Breaks down information into easy-to-digest, concise sections.
- Saves time by providing a quicker reading experience.
- Summarization algorithms are less prone to bias compared to human interpretation.
- Summarized content can improve the effectiveness of indexing.
- Helps in simplifying the decision-making process by presenting key points clearly.

## Architecture

This project utilizes **Sequence to Sequence (Seq2Seq)** modeling, employing an **Encoder-Decoder** architecture. It is primarily used for sequence-to-sequence problems where the input and output sequences have different lengths. Both the encoder and decoder are built using **Recurrent Neural Networks (RNNs)** or **Long Short-Term Memory (LSTM)** networks.

## Model Details

- The dataset is split into training and testing sets, with a 90:10 split ratio.
- The optimizer chosen is `RMSprop`.
- The model is trained for 50 epochs, with a batch size of 128 and a dropout rate of 0.4.
- **EarlyStopping** is used based on validation loss, halting the training after 35/50 epochs due to minimal improvement in validation loss.
- The model was fine-tuned by experimenting with different LSTM layer configurations and hyperparameters, including varying batch sizes (64, 128, 256, 512) and dropout rates (0.2, 0.25, 0.4).

## Performance Metrics

- **BLEU**: Bilingual Evaluation Understudy, used as the primary benchmark due to its long-standing adoption. It works by matching n-grams in the predicted summaries with those in the actual summaries.
- **GLEU**: Google’s Language Understanding Evaluation, which offers a sentence-level evaluation similar to BLEU but addresses some of its limitations.
- **METEOR**: A metric that correlates better with human judgment, using a harmonic mean of unigram precision and recall.


