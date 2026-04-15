# 🛰️ CDUWD 1.0: Chengdu Urban Waterbody Semantic Segmentation Dataset

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Paper: Remote Sens.](https://img.shields.io/badge/Paper-Remote%20Sens.-blue.svg)](https://doi.org/10.3390/rs16203873)
[![Area: Chengdu](https://img.shields.io/badge/Area-Chengdu-green.svg)](https://en.wikipedia.org/wiki/Chengdu)
[![Institution: CDUT](https://img.shields.io/badge/Institution-CDUT-red.svg)](http://www.cdut.edu.cn/)

## 🔬 1. Introduction to CDUWD 1.0
The **Chengdu Urban Water Body Semantic Segmentation Dataset (CDUWD)** is designed to address common challenges in urban water body extraction, such as incomplete boundaries, misclassification, and omission of small water bodies. 

**CDUWD** focuses on improving the accuracy of urban water body extraction for applications such as urban planning, flood management, and ecological monitoring. It provides valuable training and evaluation resources for models like **SegFormer**, enabling efficient multi-scale urban water body segmentation in complex urban environments and is applicable to various types of urban water bodies.

> [!IMPORTANT]
> The dataset is comprehensively described in the article **"Precise City-Scale Urban Water Body Semantic Segmentation and Open-Source Sample Set Construction Based on Very High-Resolution Remote Sensing: A Case Study in Chengdu,"** published in ***Remote Sens.***, which provides important support for future research on urban water resource management. The article is affiliated with **Chengdu University of Technology**.

---

## 📊 2. Source Data
The source data of the CDUWD dataset is derived from **very high-resolution (VHR)** images from Google Earth. 

| Feature | Specification |
| :--- | :--- |
| **Total Images** | 15 source images |
| **Spatial Resolution** | **0.27 meters** |
| **Spectral Bands** | Red (R), Green (G), Blue (B) |

The water body characteristics in the CDUWD dataset demonstrate the multi-scale features and variations of urban water bodies across different areas and under complex backgrounds:
* **Multi-scale features:** The images exhibit significant multi-scale features, portraying variations in water body spatial distribution and appearance.
* **Scene variability:** Water bodies display contrasting styles between urban core and peripheral areas, varying from small and regular to large and irregular shapes.
* **Complex and diverse backgrounds:** The presence of buildings and shadows complicates water body extraction, with background complexity affecting the spectral signatures and the accuracy of identification. 

---

## 📂 3. Dataset Composition and Classification
From these Source Data, **77 sample points** were selected, and **4000×4000 pixel** sample images were extracted around each point. We conducted visual interpretation and precise annotation of water bodies based on a set of criteria. 

The annotated samples were converted into raster images and underwent cropping to create two dataset versions:
* **1024 Version:** 950 samples of 1024×1024 pixels.
* **512 Version:** 3800 samples of 512×512 pixels.

### Detailed Classification:
| Subset | Type of water body | Count | Percentage (%) |
| :--- | :--- | :--- | :--- |
| **CDUWD-1** | Main rivers | 192 | 20.2% |
| **CDUWD-2** | Small rivers | 162 | 17.1% |
| **CDUWD-3** | Lakes | 288 | 30.3% |
| **CDUWD-4** | Small water | 78 | 8.2% |
| **CDUWD-5** | Others water | 57 | 6.0% |
| **CDUWD-6** | Non-water | 173 | 18.2% |

---

## 📏 4. The Labeling Principles of CDUWD
The CDUWD dataset was obtained through precise manual annotations following these core principles:
1. **Size Threshold:** Water bodies under 50 pixels were not annotated.
2. **Exclusions:** Dry riverbeds, dry ditches, and channels with unclear water presence were not annotated.
3. **Inclusions:** Ponds, artificial reservoirs, water-filled ditches, lakes, rivers, visibly flooded rice fields, and wetlands.
4. **Shadow Handling:** To maintain the accurate shape of extracted water bodies, **shadows cast by buildings on water surfaces were also marked as water bodies.**

Annotated samples were then converted to raster images for direct use in training semantic segmentation models. 

---

## 🚀 5. Download Link
The CDUWD dataset is available via the following platforms:

* **[Baidu Netdisk]** [Download Link](https://pan.baidu.com/s/1tQ2seau1Ilqo2RSt5ZBLqw?pwd=cdut) (Access code: `cdut`)
* **[Google Drive]** [Download Link](https://drive.google.com/drive/folders/1Cf0IBprLtH44uvaNPdYILF7VYOaScwPx?usp=sharing)

### Folder Structure Description:
* **`512/` folder:** Contains 3,800 samples (512×512 pixels).
* **`1024/` folder:** Contains 950 samples (1024×1024 pixels).
* **Subfolders:** Both folders contain `images/` and `labels/`, further divided into six subfolders (**CDUWD-1** to **CDUWD-6**) based on water body types.

---

## 📜 6. Article Citation Format
If you find this dataset useful for your research, please cite our official publication:

> **Cheng, X.; Zhu, Q.; Song, Y.; Yang, J.; Wang, T.; Zhao, B.; Shen, Z. Precise City-Scale Urban Water Body Semantic Segmentation and Open-Source Sampleset Construction Based on Very High-Resolution Remote Sensing: A Case Study in Chengdu. *Remote Sens.* 2024, 16, 3873. https://doi.org/10.3390/rs16203873**

---

## 🤝 7. Acknowledgements
We would like to express our sincere gratitude to the **Graduate Quality Engineering Construction Funding Program of Chengdu University of Technology (2024YAL016)** for the support of this project. We also acknowledge the efforts of all contributors, whose input and collaboration greatly contributed to the success of this research.

### Contributors & Affiliations:
* **Chengdu University of Technology:** Xi Cheng, Qian Zhu, Yujian Song, Jieyu Yang, Tingting Wang
* **Aerospace Information Research Institute (Chinese Academy of Science):** Zhanfeng Shen, Haoyu Wang
