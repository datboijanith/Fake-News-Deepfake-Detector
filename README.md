# Alethia: Uncaged
### The Reality That Won't Stay Buried: Fake News and Deepfake Detection System

### An Intelligent Multi-modal Platform to Detect Fake News, Altered Images, Fake Videos, and Cloned Voices

---

## Overview

In today's digital world, misinformation spreads faster than a wild fire. A single fake news article, a manipulated photo, or a deepfake video can reach millions of people within minutes before anyone realizing it's purely fictional. **Alethia: Uncaged** is a Python-based, AI-powered solution built to fight this plague directly, heads-on.

This project brings together **Natural Language Processing (NLP)** and **Computer Vision (CV)** into one Centralized system. In simple terms, it reads text the way a human would to judge whether it sounds truthful or misleading, and it looks at images, videos, and audio the way a trained eye would look for signs of tampering: unnatural blinking, blurred edges around a face, AI generated-sounding voice patterns, or pixel-level glitches that are invisible to the naked eye but obvious to a well-trained AI model.

The goal is simple: **give everyday users (journalists, students, fact-checkers, or curious citizens) a tool where they can paste a news article, upload an image, or drop in a video/audio file, and instantly get a clear verdict: REAL or FAKE, along with a confidence score and a visual explanation of *why* the AI thinks so.**

No AI knowledge background needed to use it. No coding knowledge required to understand the results.

---

## Why This Project Matters

Remember Michael Jackson's Tabloid Junkie song...? this is more like what he wanted from that song to this world!
- Fake news can influence elections, public health decisions, and social harmony.
- Deepfake videos and cloned voices are increasingly used for scams, blackmail, and impersonation.
- Most existing detection tools focus on only ONE type of content (either text OR images). This project combines everything into a **single, integrated pipeline**.
- It's designed to be **transparent**: instead of just saying "this is fake," it shows exactly which sentence sounds misleading or which part of an image was altered, using explainable AI techniques like **Grad-CAM heatmaps**.

---

## Key Features of this project,

### 1. Text Analysis - Fake News Detection 
- Users can paste an article, a headline, or a URL.
- The system analyzes the writing style, checks for exaggerated or emotionally manipulative language, and cross-references claims.
- Under the hood, it uses techniques like **TF-IDF**, **transformer-based embeddings (like BERT)**, and **LSTM (Long Short-Term Memory) neural networks** to understand context and detect patterns commonly found in fabricated news.
- Output: A "REAL" or "FAKE" label with a percentage confidence score, and the specific sentences flagged as suspicious.

### 2. Deepfaked Image Detection system
- The User submits a photo: for example, an AI-generated image or an Altered/Photoshopped Photo.
- The system uses **Convolutional Neural Networks (CNNs)** and advanced platform architectures like **XceptionNet** or **Vision Transformers (ViTs)** to scan the image pixel by pixel.
- It looks for tell-tale signs of manipulation: unnatural blending around the face, inconsistent lighting/shadows, or repeated pixel patterns that AI generators tend to leave behind.
- Output: A correlation heat-map overlay that visually highlights exactly which part of the image looks fake which makes a non-technical user can view the evidence, not just read a random score.

### 3. Deepfake Video Detection
- Users upload a video clip.
- The system sections/splits the video into sectioned individual frames and analyzes facial movement, blinking patterns, lip-sync accuracy, and blending artifacts across frames.
- Real human faces blink and move in naturally in various irregular ways: deepfakes often get this wrong, and the model is trained to catch it.

### 4. Generated/Computerized Voice Detection
- Users upload an audio clip or the audio track from a video.
- The system analyzes voice frequency patterns, tone consistency, and background noise artifacts to determine whether the voice was created using AI or whether it was cloned.

### 5. Real-Time Confidence Scoring
- Every prediction whether its text, image, video, or audio, comes with a clear confidence percentage (e.g., "92% likely to be FAKE") instead of a vague yes/no answer, so users understand how certain the model actually is.

### 6. Explainable AI (XAI)
- Instead of being a "black box," the system explains its reasoning:
  - For text: it underlines or highlights the specific misleading sentences.
  - For images/videos: it generates a heatmap showing exactly where the manipulation was detected.
- This builds trust and helps users learn to spot fake content themselves over time.

### 7. Simple Web Dashboard
- A clean, intuitive interface where users simply paste text, enter a URL, or drag-and-drop a media file.
- No installation of complex software needed on the user's end. Everything runs through a web browser.
- Built with a lightweight and fast backend (FastAPI) connected to an easy-to-use frontend dashboard.

---

## How It Works (In Simple Terms)

Think of the system as having two "brains" working together:

1. **The Reading Brain (NLP Pipeline)**: This part reads text like a fact-checker. It has been trained on thousands of examples of real and fake news articles, so it has learned the subtle differences in tone, structure, and word choice that separate genuine journalism from fabricated stories.

2. **The Seeing Brain (Computer Vision Pipeline)**: This part looks at images, videos, and listens to audio like a forensic analyst. It has been trained on massive datasets of real and AI-generated faces/voices, so it has learned to notice tiny inconsistencies that are nearly invisible to a human eye or ear but are mathematically obvious to a neural network.

When a user submits content, the appropriate "brain" processes it, produces a prediction, and passes the results to the dashboard along with a visual/textual explanation of its decision.

---

## Core Architecture & Technologies

| Component | Purpose | Key Technologies |
|---|---|---|
| **Text & Fake News Pipeline** | Detects linguistic manipulation, bias, and false claims | TF-IDF, Transformer Embeddings (BERT), LSTM, Large Language Models |
| **Deepfake Image/Video Pipeline** | Detects pixel-level and facial inconsistencies | CNNs, XceptionNet, Vision Transformers (ViTs) |
| **Voice/Audio Pipeline** | Detects cloned or synthetic voices | Audio feature extraction, spectrogram analysis, deep learning classifiers |
| **Explainability Layer** | Makes AI decisions transparent and understandable | Grad-CAM heatmaps, attention visualization |
| **Backend** | Handles requests, model inference, and API logic | Python, FastAPI |
| **Frontend/Dashboard** | User-facing interface for submitting content | HTML/CSS/JavaScript or a modern frontend framework |
| **Database (optional)** | Stores submission history and results | SQLite / PostgreSQL / MongoDB |

---

## Use Cases

- **Journalists & Fact-Checkers**: Quickly verify suspicious articles or viral media before publishing or sharing.
- **Social Media Platforms**: Integrate as a backend moderation tool to flag suspicious content automatically.
- **Educational Institutions**: Teach students about media literacy and how AI-generated misinformation works.
- **Everyday Users**: Anyone who receives a suspicious forwarded video, voice note, or news article can check it before believing or sharing it.

---

## Future Scope

- Browser extension for one-click verification while browsing social media.
- Mobile app version for on-the-go fact-checking.
- Multilingual support so the text pipeline can analyze fake news in regional languages, not just English.
- Real-time livestream deepfake detection for video calls and live broadcasts.
- Community-driven feedback loop where users can confirm/correct predictions to continuously improve the model.

---

## Contributing

Contributions are welcome! Whether you're experienced in machine learning, frontend development, or simply want to help improve documentation, feel free to open an issue or submit a pull request. This project is meant to grow as a community effort toward a more trustworthy digital information ecosystem.

---

## Disclaimer

This tool provides AI-generated predictions based on patterns learned from training data. While highly accurate, no detection system is 100% perfect. Results should be used as a **supporting tool for judgment**, not as absolute proof, especially in sensitive or high-stakes situations. Always cross-verify critical information through trusted, official sources.

---

## Language - Python

This entire project is built using **Python**, chosen for its rich ecosystem of AI/ML libraries (such as PyTorch/TensorFlow, Scikit-learn, Transformers, OpenCV, and FastAPI), making it ideal for building both the NLP and Computer Vision pipelines within a single, unified codebase.

---

## License

This project is licensed under **Apache License 2.0**: an open-source license that allows anyone to freely use, modify, and distribute this software, including for commercial purposes, as long as proper credit is given to the creator and Creator's copyright notices are preserved. It also provides an express grant of patent rights from contributors to users, adding an extra layer of legal protection for both developers and adopters of this project.

See the [LICENSE](LICENSE) file for the full legal text.
