## Table of Contents

- [I. Introduction](#i-introduction)
- [II. Data and Methodology](#ii-data-and-methodology)
- [III. Results](#iii-results)
- [IV. Conclusions](#iv-conclusions)

## I. Introduction
Surfing is an amazing sport that goes beyond a full-body workout. Surfing provides significant benefits for both physical and mental well-being to our bodies. However, the quality of surfing session is not determined by just wave conditions. Crowded lineups can sometimes be challenging, limiting wave access and ruining perfect sessions.

## II. Data and Methodology
This project explores how computer vision and object detection can be used to automatically detect surfers in images and videos. The dataset was obtained from Surfer Finder by AIProjects custom dataset, which can be accessed in [Roboflow](https://universe.roboflow.com/aiprojects-k0qt0/surfer-finder).


The workflow above illustrates how to implement a deep learning-based object detection system using YOLOv8. The model is trained on a custom dataset in YOLO format from Roboflow. During training, the validation set is used to monitor performance and evaluate metrics that include mAP, precision, and recall to prevent overfitting. After training is complete, the test set is used for final evaluation to measure model's performance on images. Finally, the model has been applied to images and video to detect surfers with minimum confidence set at 0.5.

## III. Results

