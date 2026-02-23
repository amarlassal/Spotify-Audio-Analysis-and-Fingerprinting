# Spotify-Audio-Analysis-and-Fingerprinting
A comprehensive Music Information Retrieval (MIR) project featuring automated genre classification for 23 musical styles, a song recommendation engine, and a custom audio fingerprinting system (Shazam-like) built with STFT and spectral peak hashing.

# Music Analysis & Audio Fingerprinting System

This repository contains a dual-phase Music Information Retrieval (MIR) project. It combines **Machine Learning** for genre classification and recommendation with **Digital Signal Processing (DSP)** to implement a robust audio identification system (similar to Shazam).

## Features

### 1. Classification & Prediction
* **Genre Classification**: Multi-class classification across 23 musical genres using a dataset of ~25,000 tracks.
* **Popularity Analysis**: Predictive modeling based on audio features like `danceability`, `energy`, and `acousticness`.
* **Conformal Prediction**: Implementation of uncertainty quantification to provide 95% confidence intervals for predictions.

### 2. Music Recommendation Engine
* **Content-Based Filtering**: Finds the 10 most similar tracks to a given song using Euclidean distance in a normalized feature space.
* **Feature Engineering**: Data preprocessing including scaling and handling class imbalances.

### 3. Audio Fingerprinting (The "Shazam" Algorithm)
A complete implementation of the *Industrial-Strength Audio Search Algorithm*:
* **STFT Processing**: Conversion of raw audio into spectrograms using `librosa`.
* **Constellation Maps**: Extraction of local spectral peaks (high-energy points).
* **Combinatorial Hashing**: Pairing "Anchor Points" with "Target Zones" to create robust hashes $(\text{freq}_1, \text{freq}_2, \Delta \text{time})$.
* **Efficient Search**: A matching engine that uses time-offset histograms to identify songs from short, noisy excerpts (5s–15s).

## 🛠️ Technical Stack
* **Language:** Python 3.x
* **Signal Processing:** `librosa`, `scipy`, `numpy`
* **Machine Learning:** `scikit-learn`, `pandas`
* **Optimization:** `numba` (for high-performance JIT compilation)

## Performance
* **Classification**: Evaluated using **Micro F1-Score**.
* **Fingerprinting**: Robust against noise and temporal shifts via relative spectral peak timing.

## Authors
This project was developed by:
* **Leon ZHU**
* **Mohamed ABDELLATIFI**
* **Amar LASSAL**

---
*Developed as part of the AARES Project (Apprentissage Artificiel pour la Reconnaissance et l'Extraction de Signaux).*
