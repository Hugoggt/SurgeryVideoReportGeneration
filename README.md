# Enhancing Surgical Documentation through Multimodal Visual-Temporal Transformers and Generative AI

This repository contains code and resources for the Master's thesis **"A Novel Multimodal Approach for Surgery Video Report Generation with Large Language Models"**.

The project has been conducted under the supervision of **Pietro Lio, Cristian Cosentino, and Mishra Siddhartha**.

---

## Introduction

### Problem Statement

Surgical procedures generate vast amounts of video data, yet extracting meaningful and structured insights from these videos remains a significant challenge. Current surgical documentation primarily relies on manual reporting, which is time-consuming, error-prone, and subject to variability among practitioners. The automatic summarization of surgical videos is crucial for improving procedural documentation, surgical training, and post-operative analysis.

### Proposed Solution

This thesis presents a **multimodal AI-driven approach** for **surgical video report generation** by leveraging **computer vision** and **large language models (LLMs)**. The model follows a structured pipeline:

1. **Video segmentation into clips**
2. **Frame-level feature extraction** using vision transformers
3. **Object detection and classification** of surgical tools, organs, and actions
4. **Frame captioning** to describe detected features
5. **Clip-level summarization** using temporal models
6. **Final structured surgical report generation** using LLMs

This approach ensures that AI can detect key instruments, actions, and critical events, producing detailed and contextually meaningful surgical summaries.

---

## Repository Structure

📂 **Repository**  
├── 📁 **Code/**   # Processed frame and clip datasets ready for training  
│   ├── `Dataset_Creation.ipynb`    # Code for dataset processing  
│   ├── `Object_Detection.ipynb`    # Object detection model  
│   ├── `Frame_Caption.ipynb`       # Frame-level caption generation  
│   ├── `Clip_Caption_Generation.ipynb`  # Clip-level captioning  
│   ├── `Summary_Generation.ipynb`  # Final report generation  
├── 📁 **Figures/**   # Figures used in the thesis                
├── 📁 **Models/**  # Fine-tuned models  
├── 📁 **Papers/**    # Research papers referenced in the thesis  
├── 📁 **Predictions/**  # Contains prediction folders of objects, frame and clip captions  
├── 📄 **Generated_Reports/**  # Reports generated for each video  
├── 📄 `LICENSE`  # Licensing information  
└── 📄 `README.md`  # Documentation and project overview   

---

## Dataset Access

Due to licensing restrictions, the original dataset cannot be shared publicly. However, access to the dataset can be requested through the following link:

- **Original Dataset**: [Google Form](https://forms.gle/GbMj8TwNoNpMUJuv9) *(Please fill out the form to request access.)*

---

## Methodology Overview

![motodol22](https://github.com/user-attachments/assets/095b3cca-f8da-49ef-b360-7e589b674a43)


### 1. **Object Detection**
- Detects surgical tools, tissues, and key structures using a **Vision Transformer (ViT)**.
- A multi-label classification approach ensures accurate feature extraction.

### 2. **Frame Captioning**
- Utilizes a **pre-trained transformer-based model** to generate text descriptions for individual frames.
- Fuses detected objects and visual context for improved text generation.

### 3. **Clip-Level Captioning**
- Leverages **Video Vision Transformers (ViViT)** for temporal modeling.
- Aggregates frame-level captions into clip-level summaries.

### 4. **Final Report Generation**
- Uses **GPT-4** to compile structured and coherent surgical reports.
- A custom prompt ensures consistency and readability in generated reports.


---

## Future Work

- **Expand the dataset** to include more surgical procedures.
- **Optimize real-time inference** to support live surgical monitoring.
- **Enhance model explainability** for better adoption in clinical practice.

For further details, please refer to the **full thesis document** in `Master_Thesis.pdf`.




