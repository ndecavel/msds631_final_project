# Automobile Make Classification of Videos

## Description

Our application is envisioned to be able to classify car makes from a video by using a variety of technologies. To do so we are implementing two main models: 1) YOLOv5 with frozen backbone layers trained on our video dataset (Berkeley DeepDrive) to detect automobiles, and 2) Car make classification model trained on the Stanford Cars Dataset. Once our models are trained, a traffic video will be inputted into the YOLO model to identify the cars and every tenth frame will be fed to the classification model to identify what make each of the automobiles are.

## Technologies Used

- YOLOv5 - https://github.com/ultralytics/yolov5
- Berkeley DeepDrive Dash-cam Dataset - https://bdd-data.berkeley.edu/
- Stanford Cars Dataset - https://www.kaggle.com/jessicali9530/stanford-cars-dataset
- Car Make Classification Model



## Demo
Here is a brief demo of our application at work. On the left is every tenth frame of an unseen dash cam video after the YOLOv5 model is applied. As one can see, the cars are identified in each frame, and those bounding box and still frames are fed into our classification model. On the right is the distribution of car makes in that particular image.
![](https://github.com/ndecavel/msds631_final_project/blob/main/images/mygif.gif)

## Instructions for use





