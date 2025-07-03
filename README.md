# Gender-Classification-Deep-Learning-Model-For-Comys-Hackathon-2025
This project, made for Comys Hackathon 2025 fine-tunes a pretrained ResNet-18 convolutional neural network to classify gender (male/female) from facial images. The model is trained using PyTorch, with custom data augmentation and class balancing strategies.
# 🚀 Hackathon Task A: Gender Recognition (Folder-wise Matching)
>  * Please download Task_A.ipynb notebook due to its huge size.
>  * Weights and biases for preatrained resnet-18 model are provided in the weightsAndBiases.txt file in details

---

## 📌 Task Objective:

> * Train a model to accurately classify the gender of a face image*

###  Success Criteria:

* if image is male , output is 1
* if image is female,output is 0                                         



## 📌 Dataset Structure:

```
/train/
    /male/
     maleX.jpg
     /female/
     femaleY.jpg

/val/
    /male/
     male1.jpg
     /female/
     female1.jpg

```
* Each folder = 1 unique individual
  Val contains persons not present in train
* male and female images are in the the training and validation folder

---

## 📌 Solution Approach (Pre-train Resnet18 model):

The approach involves the following steps:-

1. Transformed the dataset and prepare the data for pytorch
2. Due to 1623 male and 303 female images i have made weights for each sample
3. Used the pretrained resnet18
4. Training,classification,accuracy
---

## 📌 Result:

```|Final Validation Metrics (Task A - Gender Classification):
|             | precision|     recall|  f1-score|  support|

|      female|       0.79|      0.76|      0.77|        79|
|        male|       0.95|      0.95|      0.95|       343|

|    accuracy|                             0.92|       422|
|   macro avg|       0.87|      0.86|      0.86|       422|
|weighted avg|       0.92|      0.92|      0.92|       422| 
```
* Validation Accuracy: 91.71% *


## 📌 How to Run:

1.  Upload dataset to Google Colab (train + val folders)
2.  Run FaceNet Cosine Matching notebook
3.  The notebook will:

   * Evaluate val set
4.  For custom testing → Upload any image → Run final test cell

---

## 📌 Extra: Test on Any Distorted Image:

* Predicted label (1 or 0)(Male:1,Female:0)
* Try to minimize training and validation accuracy gap to prevent overfitting
---
