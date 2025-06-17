# LeukemiaClassification

## 📄 Overview
Uni project for Testing and Code Optimisation course. This project focused on testing and optimizing various aspects of Convolutional Neural Networks (CNNs) rather than creating a final high-performance classifier. The goal was to systematically compare how different settings affect training time and model accuracy.

## 🗂️ Dataset
The dataset used consists of microscopic images of blood cells, divided into two classes:
-	**ALL** — cancerous cells (Acute Lymphoblastic Leukemia)
-	**HEM** — healthy cells
A total of 15,114 images were available. For final testing and optimization, the dataset was balanced and augmented to ensure fair training without bias.

## ✅ Requirements (as per project guidelines)

The project involved:
1.	Preparing a dataset for binary classification.
2.	Training a baseline model (ResNet50) from scratch on CPU — to get reference training time and accuracy.
3.	Speed optimization by:
	 - Using GPU acceleration
	 -	Applying transfer learning
4.	Accuracy optimization by:
	  -	Adding data normalization
	  -	Applying data augmentation (including balancing classes)
	  -	Using dropout layer
	  -	Increasing training data
    -	Testing different input sizes (96×96, 160×160, 224×224)
	  -	Testing different batch sizes (32, 64, 128)
	  -	Comparing different network architectures (ResNet101, InceptionV3, DenseNet121, EfficientNetB0)

## 🔍 Main Findings
-	**_GPU + transfer learning_** greatly reduced training time and stabilized results.
-	**_Normalization and balanced augmentation_** improved validation accuracy.
-	**_Dropout_** helped control overfitting but did not directly boost accuracy.
-	**_Input size 160×160_** was the best trade-off between speed and accuracy.
-	**_Batch size 32_** provided the most stable generalization.
-	_**ResNet101**_ achieved the best accuracy overall, though with slightly longer training time compared to other architectures.

## ~ Conclusion ~
The project focused on testing and comparing different training strategies, rather than building a final production-ready classifier. Key aspects included _**effective parameter testing and clean, reusable code**_ to keep experiments organized and efficient.
