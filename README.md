# 🚀 Machine Learning & Computer Vision Engineering Portfolio

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](#)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](#)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](#)
[![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)](#)

> **M.Sc. Data Science & AI | Chalmers University of Technology**
> Specialized in Computer Vision, Deep Learning, and Geometric Modeling. I bridge the gap between academic research and production-grade ML systems, with expertise spanning from classical image processing pipelines to state-of-the-art Generative Diffusion Models. 

---

## 🌟 Featured Projects

### 1. [Generative Diffusion Models for 2D Point Clouds](https://github.com/YgggC/Image-analysis/tree/main/Project_Diffusion_models/notebooks)
**Objective:** Engineer a scalable diffusion-based neural network architecture capable of learning and generating complex 2D geometric shapes (Circle, S-curve, Swiss Roll) and joint point-cloud distributions from noise.

**Methodology & Results:**
*   **Results:** Successfully modeled complex, non-linear data distributions. The model demonstrates high-fidelity synthesis of diverse geometric shapes and captures the underlying structural manifolds of joint point clouds effectively.
*   **Methodology:** Implemented both 1D analytical diffusion processes and 2D deep learning diffusion models using **PyTorch**. The architecture leverages a reverse denoising process parameterized by a neural network. Advanced implementation includes joint point-cloud diffusion, where the model processes and denoises sets of 1024 points simultaneously, learning global shape templates rather than isolated points.

---

### 2. [Deep Learning & Logistic Classification for Cell Imaging](https://github.com/YgggC/Image-analysis/blob/main/Lab4_Learning/Learning.ipynb)
**Objective:** Develop and evaluate robust classification models for microscopic cell images and standard MNIST digit recognition tasks, establishing a comprehensive pipeline for supervised learning.

**Methodology & Results:**
*   **Results:** Achieved high classification accuracy on both tasks. Systematically evaluated the impact of weight initialization, training duration, and hyperparameter tuning on model convergence and generalization.
*   **Methodology:** Designed and trained two distinct architectures using **PyTorch**: a custom logistic classifier for biological cell images and a Convolutional Neural Network (CNN) for MNIST. The project emphasizes empirical analysis of deep learning training dynamics and model optimization.

---

### 3. [Robust 3D Reconstruction via Triangulation](https://github.com/YgggC/Image-analysis/blob/main/Lab3_3D%20reconstruction/3D%20reconstruction.ipynb)
**Objective:** Reconstruct precise 3D points from 2D image projections across multiple camera views, essential for applications in autonomous navigation and augmented reality.

**Methodology & Results:**
*   **Results:** Successfully minimized reprojection errors across complex multi-view setups, generating accurate 3D point estimations from calibrated 2D projections.
*   **Methodology:** Utilized classical geometric computer vision techniques. Formulated the pinhole camera model and solved the triangulation problem using **Nonlinear Least Squares** optimization with `SciPy`. Evaluated the robustness of the reprojection error minimization.


---

### 4. [Feature-Based Image Registration & Warping](https://github.com/YgggC/Image-analysis/blob/main/Lab2_Image%20registration/Image%20registration.ipynb)
**Objective:** Align target and source images precisely to enable seamless image stitching, multi-modal medical imaging analysis, and object tracking.

**Methodology & Results:**
*   **Results:** Achieved accurate geometric alignment between disparate image frames despite significant scale, rotation, and translation differences.
*   **Methodology:** Leveraged **OpenCV** to extract SIFT keypoints and descriptors. Implemented robust model fitting (RANSAC) to estimate geometric transformation matrices (homographies/affines), followed by pixel-level image warping.

---

### 5. [Automated Image Classification and Defect Detection](https://github.com/YgggC/Image-analysis/blob/main/Lab1_Image%20classification%20%26%20detection/Image%20classification%20%26%20detection.ipynb)
**Objective:** Build a fast, lightweight pipeline for classifying and detecting objects in images using fundamental computer vision techniques, avoiding the compute overhead of heavy neural networks.

**Methodology & Results:**
*   **Results:** Delivered a computationally efficient detection algorithm suitable for edge-device deployment, demonstrating that well-engineered classical pipelines can achieve high accuracy on specific detection tasks.
*   **Methodology:** Implemented sophisticated spatial filtering, edge detection, and morphological operations using **OpenCV** and **NumPy**. Extracted hand-crafted image features to drive the classification logic.


---

## 🔬 Limitations & Future Work

Critical analysis is essential for transitioning from research to production. Below are identified limitations and proposed architectural improvements:

**Generative Diffusion Models (Point Clouds):**
*   **Limitations:** The current implementation of the joint point-cloud diffusion scales poorly (in terms of memory and compute) if the number of points per sample significantly exceeds 1024. The self-attention mechanisms required to process the entire point cloud globally are \(O(N^2)\) complex.
*   **Future Work:** I propose integrating sparse attention mechanisms (e.g., Performer or Linformer architectures) or adopting a hierarchical latent diffusion approach. This would allow the model to scale to dense 3D LiDAR point clouds (e.g., >100k points) suitable for autonomous driving applications.

**Robust 3D Reconstruction:**
*   **Limitations:** The current nonlinear least squares solver is highly sensitive to outlier 2D matches and assumes a static scene without moving objects.
*   **Future Work:** To improve robustness, integrating an advanced robust loss function (e.g., Huber or Cauchy loss) into the optimization backend is necessary. Furthermore, coupling the triangulation module with a Graph Neural Network (GNN) could help filter out dynamic outliers before the optimization step.

---

## 🛠 Technical Stack
*   **Languages:** Python
*   **Deep Learning:** PyTorch, TorchVision, CNNs, Diffusion Models
*   **Computer Vision:** OpenCV, SimpleITK, SIFT/SURF, Feature Extraction, Geometric Modeling, Image Warping
*   **Mathematics & Data Science:** NumPy, SciPy, Matplotlib, Nonlinear Optimization, Statistical Modeling
*   **Tools:** Git, Jupyter
