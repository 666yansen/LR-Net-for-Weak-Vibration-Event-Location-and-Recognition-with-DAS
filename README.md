# LR-Net-for-Weak-Vibration-Event-Location-and-Recognition-with-DAS

This repository hosts a subset of the dataset used in the research paper "LR-Net for Weak Vibration Event Location and Recognition with DAS" (published in IEEE Sensors Journal), along with a link to the full paper. The dataset supports research on weak vibration event localization and recognition based on Distributed Acoustic Sensing (DAS) technology.

<img width="1467" height="690" alt="image" src="https://github.com/user-attachments/assets/b5bc8af0-9991-4bda-a556-37e9199563ed" />

1. Project Overview
The research focuses on solving key challenges in DAS-based vibration monitoring:
Low accuracy in multi-event simultaneous localization and recognition.
Difficulty in detecting weak vibrations (short duration, limited propagation range) which leads to high false alarm rates (NAR) and missed detection rates (MAR).
We propose an end-to-end Convolutional Neural Network (LR-Net) with two core innovations:
LAMFS (Location-Attention-Mechanism Feature Fusion and Squeeze Framework): Enhances focus on weak vibration features.
DMS (Dynamic Matching Strategy): Improves the model’s fitting ability for weak signals.

2. Dataset Details
2.1 Data Source
The dataset is collected from three typical urban IoT scenarios via field experiments:
Urban oil and gas pipelines
Highways
Industrial facilities
Sensing hardware: Ordinary armored single-mode optical cable (SMF-28e, 0.9mm polyethylene jacket) + DAS system (pulse repetition rate: 2kHz, spatial resolution: 1m).

2.2 Event Categories
The dataset includes 6 single-event categories and multi-event combinations (events co-occurring in one sample). 

2.3 Dataset Scale (Full vs. Public Subset)
The full dataset (used in the paper) includes 2227 training samples and 778 validation samples. This repository provides a public subset (focus on single-event samples to avoid redundancy/privacy issues):
    Training subset: ~350 samples (balanced across 6 single-event categories)
    Validation subset: ~150 samples


3. Full Paper Link
Access the complete research paper via IEEE Xplore:[LR-Net for Weak Vibration Event Location and Recognition with DAS](https://ieeexplore.ieee.org/abstract/document/11195999)


4. Usage Guide
4.1 Data Loading (Python Example)
Use NumPy to load the .npy time-space matrix:

4.2 Model Association
This dataset is the core input for the LR-Net model proposed in the paper. To reproduce the model’s performance:
Refer to the paper’s Section III for the LR-Net architecture (Backbone, LAMFS, DMS).
Use the dataset to train the model (Adam optimizer, focal loss for classification, smooth L1 loss for localization).

5. Contributors
The dataset and research are led by the following teams:
Nanjing University: Key Laboratory of Intelligent Optical Sensing and Manipulation (Ministry of Education), College of Engineering and Applied Sciences
Authors: Sen Yan, Ningmu Zou, Bangwei Liu, Imtiaz Naseeb Awan, Xiao Zhou, Yixin Zhang*, Xuping Zhang*
Qilu University of Technology (Shandong Academy of Sciences): Laser Institute, School of Physical Engineering
Author: Ying Shang

6. Notes
Usage Restriction: This dataset is for non-commercial research purposes only. For commercial use, contact the corresponding authors.
Data Completeness: The full dataset (including multi-event samples and raw DAS phase data) is available upon reasonable request to the authors (to protect field experiment privacy).
Issues: If you encounter data loading or format problems, submit an issue in this repository or email the corresponding authors.
