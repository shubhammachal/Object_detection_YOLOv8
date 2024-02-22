# Object_detection_YOLOv8
# Abstract
Transfer learning is a powerful technique in deep learning that allows you to leverage pre-trained models to boost the performance of object detection system. Instead of starting from scratch, we can fine tune a pre existing model, often trained on a large scale dataset, to adapt it to our specific object detection task. This approach not only saves training time and computa- tional resources but also often leads to better results.
# Introduction
Trained a yolov8 model on custom dataset that can determine, given an image, the class and location (bounding box) of objects of 3 types, according to the labels assigned in the training/validation set. While existing detection networks (e.g., SSD, Yolo, etc.) are trained for many different classes, our model was retrained to only detect three kinds of objects: car (in- cluding SUVs, vans, pick-up trucks and other small trucks), medium truck (e.g., Amazon or FedEx delivery trucks), large truck (18-wheelers, buses, cargo trucks), labeled as 1–3
# Input
For yolo input format we need one text file per image with the all the information like class label, bounding box coordintes, width and height.
# Model Selection
For our detection task we used Yolov8 which is the latest of the yolo series of models. Previously for using YOLO models, we had to download the YOLO repo and run our code from that directory. Now, we have Ultralytics packaging YOLO models as pip packages. We can easily install them by running the following command. 
<br> pip install -U ultralytics
# Model Traininig
execute following command to train the model on custom dataset <br>
!yolo task=detect mode=train epochs=3 data=custom.yaml model=yolov8n.pt batch=8 imgsz=640
