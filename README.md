# 🧠 fMRI Decoding from CNN Visual Features during Naturalistic Stimuli

This project investigates how hierarchical features extracted from a convolutional neural network (CNN), specifically VGG-16, correspond to brain activations recorded via fMRI when participants watch a movie  (a Pixar animated movie). The study bridges deep learning and neuroscience, exploring whether low- and high-level visual features align with specific brain regions.

> 🧪 Reference: Sohn, W., Di, X., Liang, Z., Zhang, Z., & Biswal, B. (2024). “Explorations of using a convolutional neural network to understand brain activations during movie watching.” *Psychoradiology*, 4, 2024.
> [https://doi.org/10.1093/psyrad/kkae021](https://doi.org/10.1093/psyrad/kkae021)

---

## 🔍 Project Summary

- **Goal**: To investigate whether CNN features extracted from a video stimulus map onto fMRI-measured brain activations.
- **Approach**: Extracted time-series features from various VGG-16 convolutional layers and used voxel-wise GLM to examine activation correspondence.
- **Significance**: Findings suggest a hierarchical alignment between CNN layers and brain regions—from low-level visual areas to high-order social regions.

---

## 🎬 Dataset

- **Source**: OpenNeuro (Dataset ID: ds000228)
- **Subjects**: 29 healthy adults (age 18–39)
- **Stimulus**: *Partly Cloudy* (Pixar short film, ~6 min)
- **fMRI Acquisition**: TR = 2s; 168 volumes; 3T Siemens scanner

---

## 🧠 CNN Model & Feature Mapping

- **Model**: Pre-trained VGG-16
- **Video Input**: Averaged 48 frames per TR (2 seconds) → 175 input frames
- **Layers Used**: 13 convolutional layers; max-pooling layers included, fully connected layers excluded
- **Feature Transformation**:
  - Averaged kernel activation maps
  - Transformed to a time series
  - Used in voxel-wise GLM and reverse analysis

![Dataset Overview](./Paper/Figure_Dataset.png)

---

## 🧪 Results Overview

| CNN Layer Depth | Brain Regions Activated                             |
| --------------- | --------------------------------------------------- |
| Layer 1         | Visual cortex, posterior cingulate (default mode)   |
| Layer 13        | Supramarginal gyrus, lateral occipital complex, STS |

- Activation patterns shift anteriorly and laterally with increasing layer depth.
- Deep-layer features correlate with high-level perceptual and social brain areas.

---

## 🔁 Reverse Analysis Insights

- **Posterior Cingulate Cortex**: Associated with kernels in Layer 1, detecting background features.
- **Visual Cortex**: Activated by kernels focusing on edges and contrast.
- **Lateral Occipital Complex**: Associated with higher-order visual processing related to object recognition.
- **Supramarginal Gyrus**: Associated with facial expression and social scenes in Layer 13.

![Dataset Overview](./Paper/Figure_Dataset.png)
![Dataset Overview](./Paper/Figure_Dataset.png)

---

## 🚧 Code

> 🚧 *The code for video preprocessing, feature extraction, and fMRI-CNN alignment analysis will be updated soon.*

---

## 📄 Citation

Sohn, W., Di, X., Liang, Z., Zhang, Z., & Biswal, B. (2024). “Explorations of using a convolutional neural network to understand brain activations during movie watching.” *Psychoradiology*, 4, 2024.
[https://doi.org/10.1093/psyrad/kkae021](https://doi.org/10.1093/psyrad/kkae021)

---

## 📬 Contact

For questions or collaboration inquiries:**Wonbum Sohn**📧 [sohnwb@gmail.com](mailto:sohnwb@gmail.com)🔗 [LinkedIn](https://www.linkedin.com/in/wonbumsohn)🌐 [www.sohnwb.com](https://www.sohnwb.com)
