# Automobile Make Classification of Videos
Nicolas Decavel-Bueff and Kyle Brooks

## Description

Our application is envisioned to be able to classify car makes from a video by using a variety of technologies. To do so we are implementing two main models: 1) YOLOv5 with frozen backbone layers trained on our video dataset (Berkeley DeepDrive) to detect automobiles, and 2) Car make classification model trained on the Stanford Cars Dataset. Once our models are trained, a traffic video will be inputted into the YOLO model to identify the cars and every tenth frame will be fed to the classification model to identify what make each of the automobiles are. We can generate a distribution of car makes within each frame, to assess if/how the distribution of car makes is changing.

## Technologies Used

- YOLOv5 - https://github.com/ultralytics/yolov5
- Berkeley DeepDrive Dash-cam Dataset - https://bdd-data.berkeley.edu/
- Stanford Cars Dataset - https://www.kaggle.com/jessicali9530/stanford-cars-dataset
- Car Make Classification Model - Resnet101 (trained on Stanford cars dataset)



## Demo
Here is a brief demo of our application at work. On the left is every tenth frame of an unseen dash cam video after the YOLOv5 model is applied. This implementation is quite successful as for the most part only the cars have green bounding boxes around them and other vehicles such as trucks do not. As one can see, the cars are identified in each frame, and those bounding boxes and still frames are fed into our classification model. On the right is the distribution of car makes resulting from our model in that particular image:

![](https://github.com/ndecavel/msds631_final_project/blob/main/images/mygif.gif)


## Next Steps
As one can see in the gif, the distribution of car models is quite inconsistent with each subsequent frame, suggesting that our classification model is having issues classifying from the dash-cam footage. We believe this may be due to the poor quality of the dash-cam videos, and as well as the fact the cars dataset primarily has images taken from the front (not like from behind in the case of the dash-cams). In the future we hope to improve accuracy in a couple of ways:
1) Add granularity as augmentation for Standford Cars dataset images to help deal with image quality issues
2) Train classification model on a different dataset or include more images of cars from behind.

## Test it yourself with your own dash-cam footage!
To generate a gif like the demo shown, use the following steps:
1) Clone this repository
2) In data directory, add the mp4 file of the dash-cam footage
3) In the 5th cell of the Final Project notebook, change the `input_video_path` variable to reflect your video path (e.g. `data/your_video.mp4`)
4) Run the notebook
5) Upon completion of the notebook, the generated gif will be in the root directory and is called `mygif.gif`







