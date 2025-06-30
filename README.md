# Object Detection and Tracking with YOLOv8 + DeepSORT
  
In this project, I built a simple but effective object detection and tracking pipeline using YOLOv8 and DeepSORT. I used Google Colab to run everything, so it's easy to try it yourself.

Basically, I upload a video, run YOLOv8 to detect objects frame by frame, and then use DeepSORT to assign each object a unique ID and track them across frames. The final output is a video with bounding boxes and IDs drawn over the objects.

## What I used
- YOLOv8n (Ultralytics) for object detection  
- DeepSORT for multi-object tracking  
- OpenCV for video processing  
- Google Colab to run it all in the cloud

## How it works
1. I upload an a 14-second clip from a security camera. There are many people moving in the video.
2. YOLOv8 detects people in each frame
3. DeepSORT tracks them by assigning unique IDs
4. OpenCV writes the processed frames into a new video called tracked_output.mp4
5. I download and view the final video

## Setup

If you want to try this yourself, you can run it in Google Colab. Just make sure to install the dependencies:

ultralytics opencv-python deep_sort_realtime

Then upload your test video and run the notebook.

## Files in this repo
- yolov8_tracking.ipynb – the main Colab notebook
- tracked_output.mp4 – sample output video
- requirements.txt – list of required packages

## Why I did this

I wanted to learn how to combine object detection with object tracking in a way that feels practical something that could work in drones, surveillance, or traffic systems. This was a fun way to explore both computer vision and AI.

## YOLOv8 detects these objects

Since I’m using the pretrained YOLOv8n model, it can recognize common objects like:
- People
- Cars, buses, trucks
- Bicycles, motorcycles
- Dogs, cats
- Anything from the COCO dataset

## Future plans
- Train on a custom dataset using Roboflow  
- Stream from a webcam instead of a file  
- Visualize object movement paths 

