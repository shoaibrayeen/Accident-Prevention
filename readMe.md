# Accident Prevention using OpenCV
![](https://forthebadge.com/images/badges/made-with-python.svg)


## Motivation

In India, there are a lot of accidents taking place every day due to mishaps. As the population grows the no. of cars and accidents is directly proportional. This example program shows how to find frontal human faces in an image and estimate their pose. The pose takes the form of 68 landmarks. These are points on the face such as the corners of the mouth, along the eyebrows, on the eyes, and so forth.

## Idea

1. We are going to implement a special method and use it to determine how long a given person’s eyes have been closed. If their eyes have been closed for a certain amount of time, we’ll assume that they are starting to doze off and play an alarm to wake them up and grab their attention.

2. Apart from this, this will also test for the same condition of yawning. In this, if the person yawns it would prompt another alert alarm for this to make him/her caution. We have also executed another extra feature by providing the driver’s parents or closed ones specifying the detailed accurate response and expressions of the driver. We have integrated the scan code with the notifications. 

3. The secured scan code which had been provided to the closed ones can easily track the facial emotions and expressions of the driver seating in the car and let’s suppose when the driver’s response is Yawning a continuous vibration notification will be sent to their closed ones cell phone stating a message “Yawning while driving” so that they can take the required measures like calling or texting him/her to prevent causing accidents.

## Working

1. We’ll set up a camera that monitors a stream for face in the vehicle in front of the driver’s seat so that we could detect and apply facial landmark localization to monitor the eyes. If a face is found, we apply facial landmark detection and extract the eye regions.

2. Now that we have the eye regions, we can compute the eye aspect ratio in which we create a function to compute the ratio of the distance between verticle eye landmarks and horizontal eye landmarks. If the eye aspect ratio indicates that the eyes have been closed for a sufficiently small amount of time, the driver will sound an alarm.

3. We are using the application of machine vision and Image processing for this purpose with the use of OpenCV, dlib, Python, and ML to implement and run our algorithm. We are using Scipy package also for the euclidean distance between facial landmark points in the eye aspect ratio calculation.

4. When a user needs information about the driver as the radius between eyelids comes closer and the driver is about to fall asleep, their closed ones will receive continous popped up notifications and tapping the secured QR code can easily be scanned through their smartphones. Through this facial emotions and expressions of the driver in the vehicle can be detected so that his/her closed ones can call him to make minute chances of causing accidents.


### Technology Used
-  Python 
-  OpenCV - Open Source Computer Vision Library is an open source computer vision and machine learning software library. A computer vision system can detect the facial emotions and detection of eye and mouth outliners in a real time video streamand then alert the driver by prompting an alarm.
-  Dlib - Dlib is a general purpose cross platform library written in the programming language in c++. It here used in detection of the facial landmark locaions. 
-  Shape Predictor 68 Face Landmarks [Trained Model]

## To Get Started

Clone the Repository
``` python
>>>  git clone https://github.com/shoaibrayeen/Accident-Prevention
```
Install required libraries
``` python
>>>  pip install -r requirements.txt
```
  
Go to src folder
``` python
>>>  cd src
```
Execute app file
``` python
>>>  python app.py
```

## Use Case of the project
- When Either no face is detected or the calculated aspect ratio is less than or equal to the threshold value, Nothing would be displayed.
- When Mouth Aspect Ratio is greater than Mouth Threshold Value, Notification for ‘Yawning’ would be displayed.
- When Eyes Aspect Ratio is greater than Eyes Threshold Value, Notification for ‘Sleeping’ would be displayed.
- When Eyes Aspect Ratio and Mouth Aspect Ratio are greater than Eyes Threshold Value and Mouth Threshold Value respectively, Notifications for ‘Sleeping and Yawning’ would be displayed.

## Data Source
- [Shape Predictor 68 Face Landmarks](http://dlib.net/face_landmark_detection.py.html)

## License
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)

**Copyright (c) 2019 Rohit Swami**

This project is licensed under the MIT License - see the LICENSE file for details

