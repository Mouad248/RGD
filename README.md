#  Emotional Analysis of Music Using Temporal Convolutional Networks (TCN)

This project focuses on **continuous emotion recognition in music** using deep learning techniques.  
Given acoustic features extracted from audio signals, the model predicts the temporal evolution of **valence**
(pleasantness) and **arousal** (emotional intensity).

The project is based on the **DEAM (Database for Emotional Analysis of Music)** dataset and implemented in **Python**
using **TensorFlow**, **openSMILE acoustic features**, and a **Temporal Convolutional Network (TCN)**.

---


##  Dataset (DEAM)

The DEAM dataset contains approximately **1,800 music excerpts**, each evaluated by **10 human annotators**.
Emotions are represented along two continuous dimensions:
- **Valence** (positivity / negativity)
- **Arousal** (emotional intensity)

Dynamic annotations are provided every **500 ms**.  
In this project, only the time interval between **15 seconds and 44 seconds** is used, as it corresponds to the
availability of emotional annotations.

Acoustic features are extracted using **openSMILE** at a temporal resolution of **0.5 seconds (2 Hz)**.

---

##  Dataset Availability

The DEAM dataset is **not included in this repository** due to its large size.

To reproduce the experiments, the dataset must be downloaded from the official source:

- **Dataset name**: DEAM (Database for Emotional Analysis of Music)  
- **Official website**: http://cvml.unige.ch/databases/DEAM/

After downloading, the dataset should be placed in the `data/` directory following the expected structure:

data/
├── features/
├── annotations/
│ └── annotations averaged per song/
│ └── dynamic (per second annotations)/


---

##  Project Structure


├── config.py # Global configuration parameters
├── main.py # Main script to run training and evaluation
├── requirements.txt # Project dependencies
├── src/
│ ├── data/
│ │ ├── loader.py # Data loading and temporal alignment
│ │ └── dataset.py # Data preprocessing and sequence generation
│ ├── models/
│ │ └── tcn_model.py # Temporal Convolutional Network architecture
│ ├── training/
│ │ └── trainer.py # Model training logic
│ └── evaluation/
│ └── evaluator.py # Model evaluation

## Contributors
This project was developed as part of a group academic project.
 . Lamia Hajjou
 . Sara Karim
 . Hajar Chaib
 . Mouad EL Mardi
