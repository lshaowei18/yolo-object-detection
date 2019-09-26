## Project title
Using YOLO object detector to detect objects in videos and images.

## Motivation
My friend and I wanted to be able to count the number of vehicles on the road real time, either using a live stream video or snapping images using a Raspberry pi.

The purpose of this repo is to share our experiences and hopefully make it a little easier for anyone who wants to explore object detection as well as working with hardwares.

## Hardware
We went to get the hardware first, purchasing a Pi NoIR Camera V2 that works with the Raspberry Pi(update the model).

List of hardware we use :
- A computer with python 2 installed
- Pi NoIR Camera V2
- Raspberry Pi
- Ethernet Cable

## Hardware Setbacks
The first setback we face was that our Raspberry Pi did not have wifi capability. This is a major setback as our initial plan was to use mobile data to connect the pi to a server.  

## Hardware Tips
Here are a few things that we learn about hardware :
- Use SSH to connect to your Pi instead of using a cable. Refer to https://www.raspberrypi.org/documentation/remote-access/ssh/
- Model of Raspberry Pi is <b>important</b>, choose wisely before starting project or purchasing one.


## Code
We decided to start with a trained model first, and we found this tutorial by Adrian Rosebrock, https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv/.

It is a YOLO(You Only Look Once) object detector that uses Deep Learning, OpenCV and Python.

The model that we used is inside the folder yolo-coco, and it contains 3 files. yolov3.weights is the weights of the model that is trained by the Darknet team.

## How to run the scripts
For images, go to the directory that contains yolo.py. Run this command: python yolo.py --image images/baggage_claim.jpg --yolo yolo-coco

The --image is to specify which image to run the model on. (In the above command, we are running on baggage_claim.jpg that is in the directory images)

For videos, the command is : python yolo_video.py --input videos/car_chase_01.mp4 --output output/car_chase_01.avi --yolo yolo-coco


## What we learn
With a trained model, object detection is not hard. However, for what we are trying to achieve, we either need faster hardware or a faster model. With a Macbook Pro, the yolo-coco model can detect at about half a second per frame. We did not test it on the Pi but we would expect it to be much slower than a Macbook Pro.

## Features
What makes your project stand out?

## Code Example
Show what the library does as concisely as possible, developers should be able to figure out **how** your project solves their problem by looking at the code example. Make sure the API you are showing off is obvious, and that your code is short and concise.

## Installation
Provide step by step series of examples and explanations about how to get a development env running.

## API Reference

Depending on the size of the project, if it is small and simple enough the reference docs can be added to the README. For medium size to larger projects it is important to at least provide a link to where the API reference docs live.

## Tests
Describe and show how to run the tests with code examples.

## How to use?
If people like your project they’ll want to learn how they can use it. To do so include step by step guide to use your project.


## Credits
Full credits to Adrian Rosebrock for the wonderful tutorial and code on pyimagesearch.com. Link to the tutorial: https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv/
