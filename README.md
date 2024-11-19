# Kaggle-CNN-Cancer-Detection
 ## Problem Description
This is a binary image classification problem where we are tasked with identifying metastatic cancer in small image patches taken from larger digital pathology scans.
The data for this kaggle mini-project is a slightly modified version of the PatchCamelyon (PCam) benchmark dataset (the original PCam dataset contains duplicate images
due to its probabilistic sampling, however, the version presented on Kaggle does not contain duplicates).

PCam is highly interesting for both its size, simplicity to get started on, and approachability

The basic problem statement is as follows:

The center region (32x32 pixels) of each image patch determines its classification:


* **1 (positive):** At least one tumor pixel in the center
* **0 (negative):** No tumor pixels in the center, even if present in the outer regions


We must predict probabilities for the test dataset and submit results in the required format for evaluation

**Evaluation Criteria:** Submissions are scored using the Area Under the Receiver Operating Characteristic Curve (ROC AUC), emphasizing the model's ability to rank predictions correctly.


## Dataset Description

In this dataset, you are provided with a large number of small pathology images to classify. The dataset provided in this competition is derived from the PatchCamelyon (PCam) benchmark dataset. The original PCam dataset contains duplicate images due to its probabilistic sampling, however, the version presented on Kaggle does not contain duplicates.


* Training Data:
    * Images: Located in the **/train** directory, each image is a small 32x32 RGB patch.
    * Labels: A CSV file (train_labels.csv) maps each image ID to a binary label (1 or 0).

* Test Data:
    * Images: Located in the **/test** directory, these patches are unlabeled and used for model prediction.
    * Submission: Predictions are uploaded in CSV format with columns id and label.

Tumor tissue in the outer region of the patch does not influence the label. This outer region is provided to enable fully-convolutional models that do not use zero-padding, to ensure consistent behavior when applied to a whole-slide image.

This dataset is available at below link:
[https://www.kaggle.com/competitions/histopathologic-cancer-detection/data](http://)
