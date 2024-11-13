
# ML Fiesta - Synergy24: Sandalwood Cultivation ASR & Question-Answering System

## Project Overview

This project aims to preserve and enhance access to indigenous knowledge on sandalwood cultivation, a significant cultural and economic resource in Karnataka, India. By leveraging Automatic Speech Recognition (ASR) and question-answering (QA) technology, we built an audio-processing pipeline that allows users to query and retrieve specific information from a dataset of Kannada audio recordings on sandalwood cultivation.

## Problem Statement

Sandalwood holds cultural and economic importance, especially in Karnataka. Our project aims to support the conservation and dissemination of information on sustainable sandalwood cultivation practices through:
1. Transcribing a Kannada-language corpus related to sandalwood.
2. Providing a QA interface that allows users to ask questions and receive targeted responses from the audio corpus.

This system assists communities in preserving and sharing knowledge about sustainable sandalwood cultivation practices.

## Dataset

The dataset consists of audio recordings about sandalwood cultivation, primarily in Kannada, gathered from YouTube. The audio files contain colloquial language and occasional background noise, requiring fine-tuned ASR to ensure accurate transcription.  
**[Dataset available here](https://onedrive.live.com/?id=BA63D4A440C2FA9%21s1b49da28d90540b8a44655eb5d8b77fb&cid=0BA63D4A440C2FA9&redeem=aHR0cHM6Ly8xZHJ2Lm1zL2YvYy8wYmE2M2Q0YTQ0MGMyZmE5L0VpamFTUnNGMmJoQXBFWlY2MTJMZF9zQnZXV2c3RF9mMDE0ZWZSSDZFVFhjLUE%5FZT13QnNMVzk)**.

## Approach and Methods

### Task 1: ASR Model Development

We developed an ASR model specifically optimized for colloquial Kannada speech on sandalwood cultivation. Here’s a breakdown of the process:

1. **Model Selection and Fine-Tuning**  
   - We utilized **OpenAI’s Whisper model** as the primary ASR model due to its multilingual and robust transcription capabilities.
   - **Helsinki-NLP’s models** were used for additional translation tasks to ensure better adaptability for the Kannada language.
   - Fine-tuning was performed using our dataset to capture dialectal expressions and colloquial nuances specific to the subject matter.

2. **Noise Handling and Filtering**  
   - We applied audio preprocessing, including noise reduction and normalization, to improve transcription quality in noisy conditions.

3. **Optimizations**  
   - Hyperparameter tuning and data augmentation techniques enhanced the model’s performance in challenging audio conditions.

### Task 2: Speech-Based Question Answering (QA)

This module enables users to ask questions in Kannada and retrieve specific information from the audio corpus. The QA pipeline was designed as follows:

1. **Question Processing and Audio-to-Text Conversion**  
   - The user’s spoken question is converted to text using the Whisper model.
   - Natural language processing (NLP) techniques identify key elements in the question to assist in information retrieval.

2. **Textual Search and Retrieval**  
   - The audio corpus is segmented and indexed after transcription. This allows the system to identify relevant segments based on the user’s query.

3. **Answer Delivery**  
   - Once a matching segment is found, the corresponding audio portion is returned, delivering an accurate answer to the user.

## Key Technologies

- **Model Framework**: OpenAI’s Whisper for ASR, Helsinki-NLP models for translation and language processing.
- **Audio Processing**: Noise reduction, normalization, and segmentation.
- **NLP Techniques**: Sentence embedding and keyword extraction for question analysis.
- **Libraries**: SpeechRecognition for ASR, PyDub for audio handling, and NLP libraries for QA processing.

## Results and Insights

The ASR and QA pipeline demonstrated high transcription accuracy for colloquial Kannada, achieving reliable retrieval of answers. This solution provides a valuable, accessible resource for promoting sustainable practices in sandalwood cultivation.

## Resources

An in-depth video tutorial on this project is available on our YouTube channel. Check it out here: **[YouTube Video](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK)**.
