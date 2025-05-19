# CerebroIQ: Multi-modal Alzheimer's Disease Detection

## Overview

CerebroIQ is a platform to help predict Alzheimer's Disease. It is a a deep learning based diagnostic architecture using MRI, PET, and co-registered brain scans to predict Alzheimer's Disease. It uses independent 3D CNN models for each imaging modality and combines them using a late fusion strategy to improve diagnostic accuracy. The project also includes a full stack medical web interface for scan uploads and predictions.

> **Note:** The website logo and the name "CerebroIQ" were generated using AI tools (ChatGPT 4.0 and DALL·E). The Flask server script used to run the backend model was also AI-assisted.

---

## Built With

* PyTorch 2.2
* Flask
* Java Spring Boot (JSP Frontend)
* Nibabel, Scikit-learn
* FSL Tools (BET, SUSAN)
* Google Colab Pro+
* IntelliJ IDEA

---

## Getting Started

These instructions will help you set up and run the complete CerebroIQ system on your local machine.

### Prerequisites

Ensure the following are installed:

* Python 3.10+
* Java 17+
* IntelliJ
* Google Colab or suitable GPU environment
* Git

### Installation

1. Running


3. Install Python dependencies:

```bash
pip install -r requirements.txt
```

4. Set up the Java Spring Boot frontend (open in IntelliJ and configure application.properties).

---

## How to Run

# Deep Learning Model (Google Colab)
1. **Create a folder** named `Final_Dataset1` in your Google Drive.

2. **Add the following subfolders** containing `.nii.gz` files:

original_mri_ad/
original_mri_cn/
augmented_mri_ad/
augmented_mri_cn/
original_pet_ad/
original_pet_cn/
augmented_pet_ad/
augmented_pet_cn/
coreg_ad_original/
coreg_ad_augmented/
coreg_cn_original/
coreg_cn_augmented/


3. **Open** `THE_3D_CNN_LATE_FUSION_MODEL.ipynb` in [Google Colab](https://colab.research.google.com).

4. **Mount Google Drive**  
In the first cell, run:
```python
from google.colab import drive
drive.mount('/content/drive')


5. pip install torch==2.2.2 nibabel==5.2.1 scikit-learn==1.4.2 pandas==2.2.2 tqdm==4.66.2 numpy==1.26.4

6. Run all cells from top to bottom to train, evaluate, and perform late fusion.















# Front end with Server
1. 


## Features

* Independent 3D CNN models for MRI, PET, and co-registered inputs
* Weighted late fusion using calibrated ensemble (RandomForestClassifier)
* REST API with JSON response
* JSP interface for clinicians to upload scans and view results
* Probability calibration to reduce overconfidence
* Integrated visual interface with AI-generated branding

---

## Acknowledgements

* [ADNI Database](https://adni.loni.usc.edu/)
* [ChatGPT & DALL·E](https://openai.com/) for logo, name and code guidance
* [FSL Toolset](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki)

---

## License

This repository is currently shared for academic use only.

---

## Contact

**Author:** \[Ravpreet Singh Gill]
**Email:** [ravpreet.s.gill@gmail.com]
**GitLab:** [https://gitlab.com/yourusername/cerebroiq]
