# 🖼️ Pengolahan Citra Digital (Digital Image Processing)

Coursework, tutorials, and a final project from my **Digital Image Processing** class — implementing image processing algorithms in Python, from pixel resampling to noise removal, morphology, and a face-mask detection pipeline built on classic (non-deep-learning) computer vision.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-image%20processing-5C3EE8?logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-array%20ops-013243?logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-SVM-F7931E?logo=scikitlearn&logoColor=white)
![Status](https://img.shields.io/badge/status-active%20coursework-brightgreen)

---

## 📚 About

This repository documents assignments, tutorials, and a final project completed for **Pengolahan Citra Digital** (Digital Image Processing). The goal throughout isn't just to call a library function and get the "right" answer — it's to understand *what's happening to the pixels*. Most operations are implemented manually (loop-level or NumPy array math) before comparing against OpenCV's built-in equivalents, to build real intuition for how each algorithm works.

## 📂 Repository Structure

```
├── assignments/       # Graded coursework — resampling, enhancement, segmentation & morphology
│   └── images/         # Sample images used across the assignments
├── tutorials/         # Hands-on / workshop notebooks from lab sessions
├── final-project/     # Face mask detection: feature extraction + SVM classifier
│   ├── dataset/         # Small sample of with_mask / without_mask training images
│   ├── ori/, mask/      # Additional sample images used in the tutorial pipeline
│   └── testing/         # Sample images for quick inference testing
├── models/            # Pretrained/reusable artifacts (Haar cascades, trained SVMs)
└── README.md
```

## 🧩 Assignments

| Notebook | Topics Covered |
|---|---|
| [`assignments/PCD_Assignment01.ipynb`](assignments/PCD_Assignment01.ipynb) | **Resampling** — Downsampling (Maximum / Average / Median methods) and Upsampling (Nearest Neighbour, Bilinear, Bicubic interpolation), with visual + quantitative analysis of each method |
| [`assignments/PCD_Assignment01_Mikail_Achmad_542370.ipynb`](assignments/PCD_Assignment01_Mikail_Achmad_542370.ipynb) | Submission version of Assignment 1 |
| [`assignments/PCD_Assignment02.ipynb`](assignments/PCD_Assignment02.ipynb) | **Image Enhancement** — correcting blurred, dark, overexposed, low-contrast, and noisy images using targeted enhancement techniques |
| [`assignments/PCD_Assignment03.ipynb`](assignments/PCD_Assignment03.ipynb) | **Segmentation & Morphology** — thresholding-based segmentation, morphological operations (erosion, dilation), and salt-and-pepper noise cleanup with before/after comparison |

Each notebook has an **"Open in Colab"** badge at the top for one-click, no-setup execution.

## 🧪 Tutorials

Hands-on lab exercises exploring additional techniques beyond the graded assignments:

| Notebook | Topics Covered |
|---|---|
| [`tutorials/Hands_On_Cell_Blood_Segmentation.ipynb`](tutorials/Hands_On_Cell_Blood_Segmentation.ipynb) | Otsu thresholding + morphology for blood cell image segmentation |
| [`tutorials/Mikail_Achmad_542370_Detection_Tutorial.ipynb`](tutorials/Mikail_Achmad_542370_Detection_Tutorial.ipynb) | Face mask detection walkthrough — dataset prep and utility functions |
| [`tutorials/Workshop_PCD_1.ipynb`](tutorials/Workshop_PCD_1.ipynb) / [`_rev.ipynb`](tutorials/Workshop_PCD_1_rev.ipynb) | In-class workshop exercises |

## 🎓 Final Project — Face Mask Detection

A classic-CV pipeline (no deep learning) that detects whether a person is wearing a face mask, using Haar cascade face detection, handcrafted feature extraction, and an SVM classifier.

| Notebook | Description |
|---|---|
| [`final-project/Training Data Face Mask.ipynb`](final-project/Training%20Data%20Face%20Mask.ipynb) | End-to-end pipeline: dataset loading → face detection → feature extraction → preprocessing → SVM training → single-image testing |
| [`final-project/Final_Project_PCD.ipynb`](final-project/Final_Project_PCD.ipynb) | Model comparison — SVM, Logistic Regression, and Random Forest |
| [`final-project/Mask Detection FIX.ipynb`](final-project/Mask%20Detection%20FIX.ipynb) | Applying the trained classifier to detect mask usage in video |

> This was a **group project**; the notebooks are included here for personal portfolio reference. The team's canonical repo (with the full video demo) lives at [kosmasrio0411/Final-Project-PCD](https://github.com/kosmasrio0411/Final-Project-PCD).

Trained artifacts and detection models used by these notebooks are in [`models/`](models/): Haar cascade XMLs for face/nose detection and the trained SVM classifiers (`.pkl`).

## 🛠️ Core Techniques Implemented

- **Geometric transforms:** image downsampling & upsampling, interpolation (nearest neighbour, bilinear, bicubic)
- **Enhancement:** brightness/contrast correction, deblurring, denoising
- **Segmentation:** intensity thresholding, Otsu's method
- **Morphology:** erosion, dilation, and noise cleanup pipelines
- **Object detection:** Haar cascade classifiers
- **Classical ML:** handcrafted feature extraction + SVM / Logistic Regression / Random Forest classification
- **Evaluation:** visual and quantitative (before/after) comparison of each method

## ⚙️ Tech Stack

- **Python 3**
- **OpenCV** (`cv2`) — image I/O, Haar cascades, and reference implementations
- **NumPy** — manual pixel/array-level algorithm implementations
- **scikit-learn** — SVM / classical ML models for the final project
- **Matplotlib** — visualization of results

## 🚀 Running the Notebooks

Assignment notebooks have an **"Open in Colab"** badge at the top — click it to run instantly in the browser. Note some notebooks expect input images to be uploaded to Colab's `/content/` directory at runtime; the source images are provided in this repo (e.g. [`assignments/images/`](assignments/images/)) for you to upload.

To run locally instead:

```bash
git clone https://github.com/mikailachmad/Pengolahan-Citra-Digital.git
cd Pengolahan-Citra-Digital
pip install opencv-python numpy matplotlib scikit-learn jupyter
jupyter notebook
```

## 👤 Author

**Mikail Achmad**
Coursework for *Pengolahan Citra Digital*

---

⭐ If you're studying image processing too, feel free to fork this and use the notebooks as a reference for your own assignments.
