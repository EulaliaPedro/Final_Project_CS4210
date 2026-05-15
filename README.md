# Knit Stitch Classifier
## CS 4210 — Applied Machine Learning Project

## Project Overview
A machine learning application that identifies stitch types from images.
Classifies two stitch types — **Stockinette** and **Single Crochet** — using 
transfer learning with ResNet-18 pretrained on ImageNet.

# How the code runs:
  This code runs on Google Colab and will not work on any other IDE
  To run:
      Step 1. Open Stitch_Classifier.ipynb at colab.research.google.com
      Step 2. Upload dataset.zip to your Google Drive root
      Step 3. Switch to T4 GPU
      Step 4. Run all cells

  The notebook will automatically:
  - Mount your Google Drive
  - Extract the dataset
  - Train the model (~10 minutes)
  - Show training curves and confusion matrix
  - Launch the prediction demo

# Required packages:
   1. Must download the dataset from: https://drive.google.com/file/d/1VppdV6VR4N2TZDjU0Z8oPChleZ1v7BPz/view?usp=sharing
   2. Download .zip folder and upload it to your Google Drive root before running the notebook
      
Where the main training, inference, or demo code is located

## Where to Find the Code

| Section | Cell | Description |
|---------|------|-------------|
| Imports | Cell 1 | All dependencies |
| Data loading | Cell 2 | Builds CSV from dataset folders |
| Transforms | Cell 3 | Resize, crop, normalize, augment |
| Dataset class | Cell 4 | CrochetDataset — loads images from CSV |
| Train/val/test split | Cell 5 | 70/15/15 split |
| Model | Cell 6 | ResNet-18 transfer learning |
| Training loop | Cell 7 | Train + validation per epoch |
| Results | Cell 8 | Loss and accuracy plots |
| Evaluation | Cell 9 | Confusion matrix + classification report |
| Stitch database | Cell 10 | Builds JSON database from dataset |
| Prediction demo | Cell 11 | Upload any image and get prediction |


## Results
- Test accuracy: **84.38%**
- Best validation accuracy: **90.32%**
- Model: ResNet-18 transfer learning
- Dataset: 207 images across 2 classes

## Dependencies

| Package | Use |
|---|---|
| PyTorch | Model training |
| torchvision | ResNet-18, transforms |
| scikit-learn | Train/val/test split, metrics |
| matplotlib / seaborn | Plots and confusion matrix |
| Pillow | Image loading |
| pandas | CSV data handling |
