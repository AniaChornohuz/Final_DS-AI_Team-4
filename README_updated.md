# Explaining Music Recommendations through Audio Features and Spectrogram Analysis  
**Final Project — Data Science & AI II**  
**Team 4: Anna-Mariia Chornohuz & Iana Schnattler**

## GitHub Repository
https://github.com/AniaChornohuz/Final_DS-AI_Team-4

---

## Project Overview

This project explores how to make music recommendations **more explainable** by combining traditional audio features with **spectrogram-based visualizations**. Our recommender system builds on two complementary approaches:

1. **Audio Feature-Based Recommender** — using interpretable features like tempo, energy, valence, etc.
2. **Spectrogram-Based Recommender** — using CNN-compatible spectrogram images to match sonic textures.

We compare both approaches in terms of recommendation performance, visual similarity, and **user interpretability**.

---

## Motivation

Most music streaming platforms offer little transparency into *why* a song is recommended. We aim to:
- Increase user **trust** through visual explanation
- Link **audio features** to perceptual patterns
- Bridge the gap between black-box AI and **human-understandable outputs**

---

## Project Structure

```
📄 Final_Project_Notebook.ipynb      ← Main workflow and modeling notebook
📄 Final_Spectrogram_Generation.ipynb ← Spectrogram generation code
📄 Final_Explainability_Visuals.ipynb ← Visualizations and interpretability
📄 Final_MP3 Download.ipynb           ← MP3 preview download + conversion
📄 dataset.csv                        ← Dataset with 100 matched tracks
📄 README.md                          ← This file
📁 spectrograms/                      ← Folder with generated spectrograms
```

---

## 🔍 Dataset

- 🎧 **Source**: Spotify datasets  
- 🔗 CSV file included: `dataset.csv`  
- Features include: `danceability`, `energy`, `valence`, `tempo`, `acousticness`, `instrumentalness`, etc.

---

## Methodology Summary

### Audio Feature Recommender
- Based on cosine similarity between feature vectors  
- Output: Top-N similar tracks + explanations like  
  _"Recommended because of similar energy and acousticness"_

### Spectrogram Recommender
- Mel-spectrograms generated from 10-second clips  
- Images analyzed using PCA / t-SNE / clustering  
- Output: Visually similar tracks with matching **sonic texture**

---

## Explainability Layer

| Feature          | Spectrogram Pattern           | Interpretation                    |
|------------------|-------------------------------|-----------------------------------|
| High Energy      | Dense high-frequency bands     | Upbeat, intense songs             |
| Low Acousticness | Harsh textures, synthetic      | Likely electronic or pop          |
| High Valence     | Bright, clean shapes           | Positive or happy songs           |

**Visualizations**:
- Top 10 spectrograms by popularity  
- Cluster maps (PCA) of audio and spectrogram features  
- Side-by-side comparisons of recommended tracks  

---

## Reproducibility Instructions

1. Clone this repo:
   ```bash
   git clone https://github.com/AniaChornohuz/Final_DS-AI_Team-4.git
   cd Final_DS-AI_Team-4
   ```

2. Install dependencies:
   - Python 3.8+
   - `librosa`, `pydub`, `scikit-learn`, `matplotlib`, `numpy`, etc.

3. Run notebooks in the following order:
   - `Final_MP3 Download.ipynb` 
   - `Final_Spectrogram_Generation.ipynb`
   - `Final_Project_Notebook.ipynb`
   - `Final_Explainability_Visuals.ipynb`

---
