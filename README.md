# CNN for Capuchinbird Sound Classification 🎵🦜

This project implements a convolutional neural network (CNN) to classify Capuchinbird calls from audio data, developed as part of the *Telecommunications* course during the **2nd semester of 2023**.

The core idea is to process `.wav` files containing audio recordings and train a model to distinguish between clips that contain Capuchinbird vocalizations and those that do not.

---

## 📁 Dataset

The dataset is divided into two folders:
- `Parsed_Capuchinbird_Clips`: Contains `.wav` files of confirmed Capuchinbird calls.
- `Parsed_Not_Capuchinbird_Clips`: Contains background bird sounds and forest ambiance that do **not** include Capuchinbird calls.

---

## 🛠️ Preprocessing

- **Resampling**: All `.wav` files are resampled from their original rate to 16kHz.
- **Spectrogram Extraction**: Audio signals are padded or truncated to 3 seconds (48,000 samples) and then transformed into spectrograms for model input.

---

## 🧠 Model Architecture

- A CNN model is trained using TensorFlow.
- Inputs: Spectrograms derived from audio files.
- Outputs: Binary classification (Capuchinbird vs. Not Capuchinbird).

---

## 📊 Evaluation

The model is trained and evaluated on labeled spectrogram data. Accuracy and performance metrics can be visualized via TensorBoard or matplotlib.

---

## 🔧 Requirements

- Python 3.x
- TensorFlow 2.x
- TensorFlow I/O
- Matplotlib

To install dependencies:
```bash
pip install tensorflow tensorflow-io matplotlib
