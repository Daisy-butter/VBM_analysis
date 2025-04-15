# Schizophrenia Classification Using VBM and Machine Learning

This repository contains the implementation and analysis of a project aimed at identifying schizophrenia-related biomarkers using voxel-based morphometry (VBM) data and machine learning models.

---

## Project Overview

The pipeline consists of three main steps:

1. **VBM Analysis**: Gray matter volume (GMV) was calculated for each participant using T1-weighted MRI scans. The results are stored in the folder `COBRE_VBM_3D`. This step is excluded from the repository, and only the processed data is provided.

2. **GLM Analysis**: A General Linear Model (GLM) was used to investigate voxel-wise differences in gray matter volume between schizophrenia patients and healthy controls. Statistical maps indicating significant differences are included in the repository.

3. **Machine Learning Model**: Based on the VBM data, a machine learning model was constructed to classify individuals as schizophrenia patients or healthy controls. The model predicts if new subjects are likely to have schizophrenia using voxel-wise GMV information as features.

---

## Folder Structure

```plaintext
.
├── COBRE_VBM_3D/          # Processed VBM data for all participants
├── GLM_Analysis/          # Output from GLM statistical analysis
│   ├── group_difference.nii.gz   # Voxel-wise statistical map
│   ├── scripts/                   # GLM implementation scripts
├── Machine_Learning_Model/  # Files related to classification model
│   ├── data_preprocessing.py     # Preprocessing pipeline for VBM data
│   ├── train_model.py            # Script for training the classifier
│   ├── predict.py                # Script for predicting diagnoses
│   ├── models/                   # Saved trained models
├── README.md            # Project documentation (this file)
