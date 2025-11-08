# 🧠 Brain Tumor Prediction Using Deep Learning

This project applies **Convolutional Neural Networks (CNN)** to detect **brain tumors** from MRI images, integrated with a **Flask web interface** for real-time prediction and a **GUI launcher** built using Tkinter.

# Quick Start & Report

The project includes a simple Tkinter launcher and a Flask web app for testing the trained model. After you download and arrange files as instructed in the repo, open the project in your Python IDE (PyCharm/VS Code) and run `app.py`. Running `app.py` opens a panel with clickable buttons (Data Preprocessing, Model Training, Model Accuracy, Brain Tumor Detection Web App, Exit). Use the GUI in this order:

1. Click **Data Preprocessing** to prepare the images and create the dataset metadata.  
2. Click **Model Training** to train the CNN. When training finishes the model will be saved to the project folder (e.g. `braintumor.h5` or `bt1.h5`).  
3. Click **Model Accuracy** to run evaluation; this shows the confusion matrix and classification report. From the latest run (confusion matrix shown in repository screenshots) the model achieved **≈ 96.45% accuracy** on the validation/test set.  
4. Click **Brain Tumor Detection Web App** from the GUI to launch the Flask app — the GUI prints (or opens) the local address. Open that address in a browser on the same machine or any device on the same local network to use the web interface.

Notes:
- Make sure you have first rearranged the dataset and other files exactly as documented in this README (Training/ and Testing/ folders, `dataset.xlsx`, model files in the project root or `/models`).  
- If you want to access the web app from another device on the same network, run the Flask app on a host address bind (e.g., `app.run(host='0.0.0.0', port=5000)`) and ensure your firewall allows connections to that port.  

This quick-start section assumes you have already followed the full setup below (virtual environment, `pip install -r requirements.txt`, dataset arrangement). Continue reading for full instructions and repository layout.

---

##  Table of Contents
---

## Table of Contents
1. Overview
2. Features
3. Folder Structure
4. Installation
5. Dataset Setup
6. Model Files
7. How to Run
8. Technologies Used
9. License & Disclaimer
10. Author


##  Overview

The **Brain Tumor Prediction** project automates brain tumor classification using MRI images.  
A CNN model trained on four tumor categories provides predictions through both:
- A **Flask web app** for image uploads and results
- A **Tkinter GUI** for local workflow control (data preprocessing, training, accuracy visualization, and web app launch)

###  Tumor Classes:
- Glioma Tumor  
- Meningioma Tumor  
- Pituitary Tumor  
- No Tumor  

---

## 🚀 Features

- Deep Learning-based CNN model for multi-class tumor detection  
- Flask web interface for MRI upload & classification  
- Tkinter desktop interface for preprocessing, training, and evaluation  
- Organized dataset and Excel metadata structure  
- Matplotlib performance plots (Loss & Accuracy)  
- Confusion matrix & classification report visualization  
###Confusion Matrix
<p align="center">
  <img src="static\Screenshot 2025-11-09 020148.png" width="600" alt="Confusion Matrix">
  <img src="static\Screenshot 2025-11-09 020513.png" width="600" alt="Confusion Matrix">
</p>

---
## 📂 Folder Structure
<pre><code>
Brain_Tumor_Prediction/
│
├── app.py                 # Flask web application
├── cnn.py                 # CNN model training script
├── cnnacc.py              # Model evaluation & accuracy visualization
├── preprocessing.py       # Data preprocessing script
├── Home.py                # GUI launcher using Tkinter
│
├── braintumor.h5          # Trained model (main)
├── bt.h5                  # Alternate model
├── bt1.h5                 # Alternate model
├── dataset.xlsx           # Image metadata file (paths & labels)
│
├── Training/
│   ├── glioma_tumor/
│   ├── meningioma_tumor/
│   ├── pituitary_tumor/
│   └── no_tumor/
│
├── Testing/
│   ├── glioma_tumor/
│   ├── meningioma_tumor/
│   ├── pituitary_tumor/
│   └── no_tumor/
│
├── static/
│   ├── css/
│   ├── js/
│   ├── img/
│   │   ├── brain.jpg
│   │   └── braintumor1.webp
│
├── templates/
│   ├── index.html
│   └── result.html
│
├── uploads/
├── fonts/
│
├── requirements.txt
├── LICENSE
└── README.md
</code></pre>



## Installation
1. Clone the repository:
  <a href="git clone https://github.com/AdityaPande-ML-DataAnalyst/Brain_Tumor_Prediction.git
cd Brain_Tumor_Prediction"></a>

##2.Create and activate a virtual environment:
- python -m venv venv
- venv\Scripts\activate 
## 3.Install all required dependencies:
pip install -r requirements.txt
Dataset Setup
This project uses an Excel file (dataset.xlsx) to store image paths and labels for all MRI images. The Excel file should have the following structure:
 Path	 | label |
|----------|--------------|
| **Training/glioma_tumor/image001.jpg** | glioma_tumor |
| **Training/meningioma_tumor/image002.jpg** | meningioma_tumor |
| **Training/no_tumor/image003.jpg	** | no_tumor | 
| **Training/pituitary_tumor/image004.jpg** | pituitary_tumor | 


## folder should be 
<pre><code>
Training/
│   ├── glioma_tumor/
│   ├── meningioma_tumor/
│   ├── pituitary_tumor/
│   └── no_tumor/
Testing/
│   ├── glioma_tumor/
│   ├── meningioma_tumor/
│   ├── pituitary_tumor/
│   └── no_tumor/
</code></pre>

##Technologies use 
Category | Tools |
|----------|--------------|
|Language|	Python 3.x|
|Deep Learning	|TensorFlow, Keras
|Web Framework|	Flask
|Image Processing|	OpenCV, Pillow
|Data Analysis|	Pandas, NumPy, Scikit-learn
|Visualization|	Matplotlib, Seaborn, LivelossPlot
|GUI	|Tkinter|


License & Disclaimer
License: MIT License
You are free to use, modify, and distribute this project with attribution.

Disclaimer:
This project is for educational and research purposes only.
It is not a certified medical diagnostic tool and must not be used for clinical or medical decisions.
No identifiable patient data is included.

Author
Aditya Pande
📧<a herf = "adityapande831@gmail.com"></a>



