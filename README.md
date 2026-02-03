## Table of Contents

- [I. Introduction](#i-introduction)
- [II. Data and Methodology](#ii-data-and-methodology)
- [III. Results](#iii-results)
- [IV. Conclusions](#iv-conclusions)

## I. Introduction
Surfing is an amazing sport that goes beyond a full-body workout. Surfing provides significant benefits for both physical and mental well-being to our bodies. However, the quality of surfing session is not determined by just wave conditions. Crowded lineups can sometimes be challenging, limiting wave access and ruining perfect sessions.

## II. Data and Methodology
This project explores how computer vision and object detection can be used to automatically detect surfers in images and videos. The dataset was obtained from Surfer Finder by AIProjects custom dataset, which can be accessed in [Roboflow](https://universe.roboflow.com/aiprojects-k0qt0/surfer-finder).

<p align="center">
  <img width="400" height="350" src="https://github.com/a-pradono/surfer_object_detection/blob/main/images/workflow.png">
</p>

The workflow above illustrates how to implement a deep learning-based object detection system using YOLOv8. The model is trained on a custom dataset in YOLO format from Roboflow. During training, the validation set is used to monitor performance and evaluate metrics that include mAP, precision, and recall to prevent overfitting. After training is complete, the test set is used for final evaluation to measure model's performance on images. Finally, the model has been applied to images and video to detect surfers with minimum confidence set at 0.5.

## III. Results
The first figure below summarizes YOLOv8 losses and metrics. Since our data only has one class only, there are no class mis-identifications and the classification error is constantly zero. 

<p align="center">
  <img width="700" height="400" src="https://github.com/a-pradono/surfer_object_detection/blob/main/images/losses_metrics.png">
</p>

The Precision-Recall (PR) curve is used to evaluate performance by visualizing the trade-off between precision and recall at different thresholds. The curve shows 0.918 mAP@0.5, which means the mean Average Precision (maP) at IoU (Intersection over Union) threshold of 0.5.

<p align="center">
  <img width="400" height="400" src="https://github.com/a-pradono/surfer_object_detection/blob/main/images/pr_curve.png">
</p>

Once satisfactory training performance was achieved, the trained model was used for inference on test dataset. Here are some sample of the test predictions on unseen images.

<p align="center">
  <img width="450" height="450" src="https://github.com/a-pradono/surfer_object_detection/blob/main/images/surfer_image.png">
</p>

Now, let's see how the model performs on video. By running the detector on video footage, surfers can be automatically detected in real time. With a live beach camera, this approach could give a quick insights of how crowded the lineup is before heading out for a great surf session.

<p align="center">
  <img width="500" height="400" src="https://github.com/a-pradono/surfer_object_detection/blob/main/images/surfer_video.gif">
</p>

## IV. Conclusions
The objective of this project was to explore the use of computer vision models for detecting surfers using YOLO. These are the conclusions drawn from this project:
  * The custom dataset exported from Roboflow in YOLOv8 format simplified data preparation process.
  * YOLOv8 model proved to be an efficient model for detecting surfers with an mAP@0.5 of 0.918.
