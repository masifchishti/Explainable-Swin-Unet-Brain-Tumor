# Explainable-Swin-Unet-Brain-Tumor
Official implementation of Hybrid Swin-Unet for Brain Tumor Detection with Grad-CAM Explainability

Explainable Hybrid Neural Networks for Trustworthy Brain Tumor Detection

This repository contains the implementation of a Hybrid Swin-Unet architecture for multi-class brain tumor classification from MRI scans. The model integrates hierarchical Swin Transformers with a U-Net decoder to capture both global context and local spatial features.

Key Features:

1.	Hybrid Swin-Unet Architecture: Combines transformer-based global modeling with CNN-like local feature recovery.
2.	Weighted Random Sampling (WRS): Addresses class imbalance across Glioma, Meningioma, and Pituitary tumor types.
3.	Explainable AI (XAI): Integrated Grad-CAM heatmaps for clinical validation and transparency.
4.	High Performance: Achieves 97.94% accuracy on the benchmark Brain Tumor MRI dataset.

Installation:

1.	Clone the repository:
2.	git clone https://github.com/yourusername/Explainable-Swin-Unet-Brain-Tumor.git
3.	cd Explainable-Swin-Unet-Brain-Tumor
4.	Install dependencies:
5.	pip install torch torchvision numpy matplotlib seaborn scikit-learn

How to Run:

1. Training and Evaluation

To train the model and generate performance metrics (Confusion Matrix, ROC, etc.):
python main_training.py

2. Generate Grad-CAM Heatmaps

To visualize the model's decision-making on a specific MRI slice:
python visualize_gradcam.py --image_path path/to/mri_image.jpg

Results Summary:

	Accuracy: 97.94%
	Mean AUC: 0.98
	Inference Time: 28ms (NVIDIA Tesla T4)

Visual Results

Grad-CAM Explainability

The model provides explainable predictions using Grad-CAM heatmaps to highlight important MRI regions influencing the decision.

Model Performance

Performance evaluation includes accuracy curves, confusion matrix, ROC analysis, and prediction visualization.

Repository Structure:

	model/: Swin-Unet architecture definition.
	utils/: Data loaders, preprocessing, and WRS implementation.
	results/: Saved high-resolution figures (PNG).
	weights/: Trained model checkpoints.

License:

This project is licensed under the MIT License - see the LICENSE file for details.
