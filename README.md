# CerebroIQ: Multi-modal Alzheimer's Disease Detection

## Overview

CerebroIQ is a deep learning based diagnostic framework that leverages MRI, PET, and co-registered brain scans to predict Alzheimer's Disease. It uses independent 3D CNN models for each imaging modality, combining them using a calibrated late fusion strategy to enhance diagnostic accuracy. The project also includes a full stack medical web interface for scan uploads and predictions.

> **Note:** The website logo and the name "CerebroIQ" were generated using AI tools (ChatGPT 4.0 and DALL·E). The Flask server script used to run the backend model was also AI-assisted. In addition thorough code checks were conducted too.

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

1. Clone the repository:

```bash
git clone https://gitlab.com/yourusername/cerebroiq.git
cd cerebroiq
```


3. Install Python dependencies:

```bash
pip install -r requirements.txt
```

4. Set up the Java Spring Boot frontend (open in IntelliJ and configure application.properties).

---

## How to Run


# here write how to 


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
