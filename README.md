# AI-BASED-SMART-PORTABLE-SKIN-CANCER-PRE-SCREENING-DEVICE
AI-based portable skin cancer pre-screening device using ESP32-CAM, image processing, and machine learning to provide preliminary skin-lesion risk assessment for low-resource and rural healthcare settings.
# 🩺 AI-Based Smart Portable Skin Cancer Pre-Screening Device

An **AI-based smart portable skin cancer pre-screening device** designed to capture images of suspicious skin lesions and provide a preliminary risk assessment using **ESP32-CAM, image processing, and machine learning/deep learning techniques**.

The project focuses on developing a **low-cost, portable, and easy-to-use prototype** that can support preliminary screening, particularly in **rural and low-resource healthcare environments**.

> ⚠️ **Disclaimer:** This prototype is intended for educational and research purposes only. It is a pre-screening system and does not replace professional medical diagnosis, biopsy, or examination by a qualified healthcare professional.

---

## 📌 Project Overview

Skin cancer can be easier to manage when suspicious lesions are identified and evaluated at an early stage. However, access to dermatologists and advanced diagnostic equipment may be limited in rural and resource-constrained areas.

This project proposes a compact device that combines:

* 📷 **ESP32-CAM** for image acquisition
* 💡 **White LED ring illumination** for controlled lighting
* 🧠 **AI/ML model** for preliminary image-based risk assessment
* 🖥️ **OLED display** for displaying the screening result
* 🔋 **Rechargeable battery** for portable operation
* 📡 **Wi-Fi connectivity** for image/data transfer when required

The captured skin image can be processed using computer vision and an AI model trained on publicly available skin-lesion datasets.

---

# 🎯 Objectives

The major objectives of this project are:

1. To design a **portable skin-lesion image acquisition device**.
2. To capture images under controlled illumination.
3. To preprocess the captured images for AI analysis.
4. To develop/train an AI model for preliminary skin-lesion classification or risk assessment.
5. To display the output through an OLED screen.
6. To develop a low-cost prototype suitable for research and educational demonstrations.
7. To explore the potential use of AI-assisted screening in rural and low-resource environments.

---

# 💡 Proposed Solution

The proposed system follows the workflow:

```text
        👤 Skin Lesion
             │
             ▼
     📷 ESP32-CAM Camera
             │
             ▼
      💡 LED Illumination
             │
             ▼
      🖼️ Image Capture
             │
             ▼
     🔧 Image Preprocessing
             │
             ▼
       🧠 AI/ML Model
             │
             ▼
      📊 Risk Assessment
             │
             ▼
        🖥️ OLED Display
             │
             ▼
     Preliminary Result
```

---

# 🔬 System Architecture

```text
 ┌───────────────────────┐
 │     Skin Lesion       │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │   White LED Ring      │
 │   Controlled Lighting │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │      ESP32-CAM        │
 │   Image Acquisition   │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │ Image Preprocessing   │
 │ Resize / Normalize    │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │      AI Model         │
 │ CNN / ML Classifier   │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │   Risk Assessment     │
 └───────────┬───────────┘
             │
             ▼
 ┌───────────────────────┐
 │     OLED Display      │
 │   Low / Medium / High │
 └───────────────────────┘
```

---

# ⚙️ Hardware Components

| Component                | Purpose                                    |
| ------------------------ | ------------------------------------------ |
| ESP32-CAM                | Image acquisition and embedded control     |
| OV2640/compatible camera | Captures skin-lesion images                |
| OLED 0.96" I²C           | Displays screening result                  |
| White LED Ring           | Provides controlled illumination           |
| 18650 Li-ion Battery     | Portable power source                      |
| TP4056                   | Battery charging/protection                |
| MT3608 Boost Converter   | Boosts battery voltage for required supply |
| N-Channel MOSFET         | Controls LED illumination                  |
| Push Button              | User input/control                         |
| ON/OFF Switch            | Main power control                         |
| Resistors                | Current limiting and signal control        |
| Capacitors               | Power filtering and stability              |
| Perfboard/PCB            | Hardware assembly                          |
| USB-to-TTL Programmer    | ESP32-CAM programming                      |

---

# 🧠 AI / Machine Learning

The AI component is intended to analyze captured skin-lesion images and provide a **preliminary risk classification**.

Possible model workflow:

```text
Dataset
   ↓
Image Collection
   ↓
Image Cleaning
   ↓
Preprocessing
   ↓
Resize Images
   ↓
Normalization
   ↓
Data Augmentation
   ↓
Model Training
   ↓
Validation
   ↓
Testing
   ↓
Performance Evaluation
   ↓
Deployment / Prototype Integration
```

---

# 📚 Dataset

The project can use publicly available dermatology image datasets for research and model development.

Potential datasets include:

* **ISIC – International Skin Imaging Collaboration**
* **HAM10000 – Human Against Machine with 10000 training images**

The dataset should be appropriately divided into:

```text
Training Dataset
        │
        ├── Training Images
        │
        └── Validation Images

Testing Dataset
        │
        └── Unseen Images
```

Dataset information, preprocessing steps, and source details are documented separately in:

```text
ai-model/dataset/dataset-info.md
```

---

# 🧪 Image Preprocessing

Before feeding images into the AI model, preprocessing may include:

### 1. Image resizing

Images are converted to a fixed input size required by the model.

Example:

```text
Original Image
      ↓
Resize
      ↓
224 × 224 pixels
```

### 2. Normalization

Pixel values can be normalized to improve model training.

### 3. Noise reduction

Image processing techniques can be applied to reduce unwanted noise.

### 4. Data augmentation

Training images may be augmented using:

* Rotation
* Horizontal/vertical flipping where appropriate
* Cropping
* Scaling
* Brightness variation

This can help the model learn from variations in image appearance.

---

# 🧠 AI Model

A CNN-based approach can be explored for skin-lesion image classification.

Example architecture:

```text
Input Image
     ↓
Convolution Layer
     ↓
Activation
     ↓
Pooling
     ↓
Convolution Layer
     ↓
Pooling
     ↓
Feature Extraction
     ↓
Fully Connected Layer
     ↓
Classification
     ↓
Risk Assessment
```

For resource-constrained hardware, lightweight architectures or **transfer learning** can be considered.

Possible models include:

* CNN
* MobileNet
* MobileNetV2
* EfficientNet
* TensorFlow Lite models

The final model should be selected based on its accuracy, computational requirements, memory usage, and suitability for the target hardware.

---

# 📊 Risk Assessment

The prototype can present a simple preliminary risk indication.

Example interface:

```text
┌─────────────────────┐
│   SKIN SCREENING    │
│                     │
│   Risk: LOW         │
│                     │
│   20–40%            │
└─────────────────────┘
```

```text
┌─────────────────────┐
│   SKIN SCREENING    │
│                     │
│   Risk: MEDIUM      │
│                     │
│   60–70%            │
└─────────────────────┘
```

```text
┌─────────────────────┐
│   SKIN SCREENING    │
│                     │
│   HIGH RISK         │
│                     │
│   ≥80%              │
│ Please consult      │
│ a doctor             │
└─────────────────────┘
```

**Important:** These percentage ranges are prototype/UI categories, not clinically validated probabilities. A model's raw confidence score should not be presented as a medically established cancer probability without clinical validation and calibration.

---

# 🖥️ OLED Output

The OLED can display:

```text
Initializing...
       ↓
Camera Ready
       ↓
Capture Image
       ↓
Analyzing...
       ↓
Risk: LOW
```

or:

```text
Risk: MEDIUM
Monitor / Evaluate
```

or:

```text
HIGH RISK
Consult Doctor
```

The displayed result should be treated as a **screening indication only**.

---

# 📡 ESP32-CAM

The ESP32-CAM acts as the main image acquisition controller.

Main functions:

* Camera initialization
* Image capture
* Wi-Fi communication
* Data transfer
* Peripheral control
* OLED communication
* LED illumination control

Example software flow:

```text
ESP32-CAM Boot
      ↓
Initialize Camera
      ↓
Initialize OLED
      ↓
Turn ON Illumination
      ↓
Capture Image
      ↓
Process / Transfer Image
      ↓
AI Analysis
      ↓
Receive Result
      ↓
Display Result
```

---

# 💡 Illumination System

Consistent lighting is important for image acquisition.

A white LED ring can be positioned around the camera to provide relatively uniform illumination.

```text
       💡 💡 💡
    💡    📷    💡
       💡 💡 💡

       Skin Lesion
```

The LED ring can be controlled using an N-channel MOSFET so that the ESP32-CAM does not directly drive a high-current LED load.

---

# 🔋 Power System

The portable power section consists of:

```text
18650 Li-ion Battery
        │
        ▼
     TP4056
 Charging + Protection
        │
        ▼
   MT3608 Boost
        │
        ├────────► ESP32-CAM
        │
        └────────► LED / Other Load
```

The exact supply voltage and current requirements should be verified for each component before assembling the final prototype.

---

# 💻 Software Requirements

Possible software tools:

* Arduino IDE
* Visual Studio Code
* Python
* OpenCV
* TensorFlow / TensorFlow Lite
* NumPy
* Matplotlib
* Git
* GitHub

---

# 📁 Project Folder Structure

```text
📦 AI-Smart-Portable-Skin-Cancer-PreScreening
│
├── 📄 README.md
│
├── 📁 hardware
│   ├── 📁 circuit-diagram
│   ├── 📁 breadboard-connection
│   ├── 📄 component-list.md
│   └── 📁 hardware-photos
│
├── 📁 software
│   ├── 📁 esp32_camera
│   ├── 📁 oled_display
│   └── 📁 wifi
│
├── 📁 ai-model
│   ├── 📁 preprocessing
│   ├── 📁 training
│   ├── 📁 evaluation
│   └── 📁 model
│
├── 📁 images
│
├── 📁 documentation
│
├── 📁 results
│
├── 📄 requirements.txt
│
└── 📄 LICENSE
```

---

# 🚀 How to Run the Project

## Step 1 — Hardware Setup

Connect the:

* ESP32-CAM
* Camera
* OLED
* LED ring
* MOSFET
* Battery
* TP4056
* Boost converter
* Switch

according to the circuit diagram provided in the `hardware` folder.

---

## Step 2 — ESP32-CAM Setup

Install:

* Arduino IDE
* ESP32 board package
* Required camera libraries
* OLED library

Select the appropriate ESP32-CAM board from the Arduino IDE.

Upload:

```text
software/esp32_camera/esp32_camera.ino
```

---

## Step 3 — OLED Setup

Upload:

```text
software/oled_display/oled_display.ino
```

and verify that the OLED initializes correctly.

---

## Step 4 — AI Environment

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Typical libraries may include:

```text
numpy
opencv-python
tensorflow
matplotlib
scikit-learn
pillow
```

---

## Step 5 — Dataset Preparation

Place the appropriately licensed dataset in the dataset directory and perform:

```text
Data Collection
      ↓
Data Cleaning
      ↓
Preprocessing
      ↓
Train / Validation / Test Split
      ↓
Model Training
```

---

## Step 6 — Model Training

Run the training script from:

```text
ai-model/training/
```

The trained model can then be evaluated using unseen test images.

---

# 📈 Model Evaluation

The model should be evaluated using appropriate metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix
* Sensitivity
* Specificity
* ROC-AUC where appropriate

Example:

```text
                Predicted
              Positive  Negative
Actual
Positive         TP        FN
Negative         FP        TN
```

Accuracy alone should not be used to judge a medical screening model, particularly when the dataset contains class imbalance.

---

# 🔬 Testing

Testing can be performed at multiple levels.

### Hardware Testing

* Camera initialization
* Image capture
* OLED display
* LED illumination
* Battery operation
* Wi-Fi communication

### Software Testing

* Image preprocessing
* Model loading
* Prediction
* Result generation
* OLED output

### System Testing

```text
Capture
   ↓
Process
   ↓
Predict
   ↓
Display
```

The complete pipeline should be tested using images that were not used during model training.

---

# 📷 Prototype

Add your actual prototype photographs inside:

```text
images/
```

Recommended photographs:

```text
prototype-front.jpg
prototype-side.jpg
prototype-inside.jpg
esp32-camera.jpg
oled-output.jpg
```

Then display the main prototype image in the README:

```markdown
![Prototype](images/prototype.jpg)
```

---

# 🌍 Potential Applications

The concept can be explored for:

* Rural healthcare screening
* Community health camps
* Preliminary skin-lesion screening
* Healthcare awareness programs
* Medical engineering research
* AI-assisted image analysis research
* Educational biomedical prototypes

The device is intended to support **preliminary screening**, not to replace professional diagnosis.

---

# ⭐ Key Features

* 📱 Portable design
* 📷 ESP32-CAM image acquisition
* 💡 Controlled illumination
* 🧠 AI-based image analysis
* 🖥️ OLED result display
* 🔋 Battery-powered operation
* 📡 Optional Wi-Fi communication
* 💰 Low-cost prototype approach
* 🌍 Potential suitability for resource-limited environments

---

# 🔮 Future Improvements

Future versions can include:

1. Higher-resolution camera modules.
2. Better controlled illumination.
3. Larger and more diverse datasets.
4. Clinically validated datasets.
5. Lightweight edge-AI models.
6. TensorFlow Lite / TinyML deployment.
7. Mobile application integration.
8. Cloud-based data management with appropriate privacy safeguards.
9. Secure patient-data handling.
10. Model calibration and clinical validation.
11. Improved enclosure and ergonomic design.
12. Additional skin-lesion categories.
13. Offline AI inference for areas with limited connectivity.

---

# ⚠️ Limitations

The current prototype has several limitations:

* The system is not a clinically approved diagnostic device.
* Dataset quality directly affects model performance.
* Lighting and camera positioning can influence predictions.
* AI confidence does not automatically represent actual disease probability.
* The prototype requires further testing using clinically representative data.
* Clinical validation is required before any real-world medical deployment.

---

# 🧑‍💻 Technologies Used

```text
Hardware
├── ESP32-CAM
├── Camera Module
├── OLED
├── LED Ring
├── Li-ion Battery
├── TP4056
└── MT3608

Software
├── Arduino IDE
├── Python
├── OpenCV
├── TensorFlow
├── NumPy
├── Scikit-learn
└── Git/GitHub

AI
├── Image Preprocessing
├── CNN / Transfer Learning
├── Classification
└── Model Evaluation
```

---

# 📚 References

Suggested references and dataset sources should be added here after finalizing the exact papers and datasets used in the project.

Example format:

```text
[1] International Skin Imaging Collaboration (ISIC), Skin Image Dataset.

[2] Tschandl, P. et al., "The HAM10000 dataset, a large collection of multi-source dermatoscopic images of common pigmented skin lesions."

[3] Relevant CNN / transfer-learning research paper used for model development.

[4] Relevant ESP32-CAM technical documentation.

[5] Relevant image-processing or computer-vision research paper.
```

---

# 🤝 Contribution

Contributions and suggestions are welcome.

If you would like to contribute:

```bash
git clone <repository-url>
```

Create a new branch:

```bash
git checkout -b feature/new-feature
```

Commit your changes:

```bash
git add .
git commit -m "Add new feature"
```

Push the branch:

```bash
git push origin feature/new-feature
```

Then create a Pull Request.

---

# 📜 License

This project can be released under the MIT License for educational and research use.

Add the appropriate license file before publishing the repository.

---

# 👩‍💻 Author

**HemaPriya Govindan**

Biomedical Engineering Student
Interested in **Biomedical Technology, Artificial Intelligence, Computer Vision, and Software Development**

---

## ⭐ Project Summary

**AI-Based Smart Portable Skin Cancer Pre-Screening Device** combines biomedical engineering, embedded systems, computer vision, and artificial intelligence to explore a portable approach for preliminary skin-lesion screening.

The project demonstrates how **ESP32-CAM + controlled illumination + image processing + AI + OLED output** can be integrated into a compact biomedical engineering prototype.

> **Capture → Process → Analyze → Display → Support Early Screening**
