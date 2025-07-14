# Coreset Distillation Experiments

This repository contains experiments and implementations related to **coreset distillation techniques** in machine learning. Coreset distillation is a method used to reduce large datasets into smaller, representative subsets (coresets) that preserve essential information for training deep learning models.

## 🚀 Purpose

The goal of this project is to **test, evaluate, and improve coreset distillation methods** for scalable and efficient model training, particularly in security-focused domains like **IoT network traffic analysis**.

## 🧪 Features

- Implementation of various coreset selection strategies
- Support for the **CIC IoT 2023** dataset (Canadian Institute for Cybersecurity)
- Evaluation of coreset quality in the context of **anomaly and intrusion detection**
- Integration with popular deep learning frameworks (e.g., PyTorch, TensorFlow)
- Reproducible experiment scripts and configurations

## 🛠 Techniques Explored

- K-Center Greedy 
- Gradient Matching
- Feature-selection (Importance based selection)
- Clustering-based Selection (Gaussian Mixture Models)
- Submodular Optimization

## 📝 NOTES: 
-Dataset in use: [CIC IOT 2023](https://www.unb.ca/cic/datasets/iotdataset-2023.html), or you can use the version with balanced sample counts under `Dataset_distilled` folder
Except for the baseline version (base_line_traditional_machine_learning.ipynb) , all further training used the distilled feature version of the original dataset under `Dataset_distilled` folder

## 📁 Directory Structure
- Dataset_distilled: contains 2 version of the original dataset, `dataset.csv` is the one with balanced sample count across classes and `dataset_distilled.csv` is the one with reduced feature set using feature selection based on importance.
- feature_selection.ipynb: using the feature-distilled dataset based on features' importance to reduce the dimension of the feature set.
- Instance_selection_KNN.ipynb: using K-Center approach to select the X nearest samples to the centroid of each class.
- distribution_matching_GaussianMixture.ipynb : using Gaussian Mixture to synthesize new samples with reduced count but aims to retains the same amount of knowledge.
- PCA.ipynb: using principle component analysis technique to further reduce the feature set.
- GAN.ipynb: not working, sad 😭
