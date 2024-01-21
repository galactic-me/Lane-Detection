# Lane-Detection
Lane Detection is an Image Segmentation problem. As the name suggests, the task of image segmentation is to partition the image into regions. There are mainly two techniques for lane identification namely: lane-mark detection and road region segmentation. This project uses Lane mark detection for lane identification. 

Here, using deep learning , I have used transfer learning and re-trained a pretrained Neural
Network named U Net.
IMAGE SEGMENTATION:
It is used to detect objects and boundaries in an image frame. With this technique, labels
are assigned to each pixel of an image such that pixels with same labels can be
characterised and classified.
It contains majorly two different parts: Object Detection and Semantic Segmentation.

DATASET USED(TUsimple):
It consists of 3,626 training sets ad 2,782 testing datasets. It consists datasets of the
highway environment. Accuracy is the main evaluation point there. The resolution of each
image is 1280 x 720. Images are under different weather conditions.
Dataset & Documentation Link:
https://www.kaggle.com/datasets/manideep1108/tusimple/data

METHODOLOGY:
(1) DATA COLLECTION: Here the dataset used is TuSimple Dataset. It is a publicly
available dataset that was released as a part of TuSimple Lane Detection Challenge. It
contains 3626 videos of 1 second each. Each of these video clips contain 20 frames, of
which the last frame is annotated.

(2) DATASET VISUALISATION: Data can be visualized using matplotlib.pyplot library. Cv2
library will be used to view the images. To visualize the lanes, we will use json library.

(3) Generating Labelled Images : We have to generate label images for json files. They
can be generated using OpenCV by drawing lines passing through the points in JSON file.
OpenCV’s polylines method can be used here. Generate a mask image using the same.

(4) BUILD AND TRAIN MODEL: We will use a pre-trained model PINet as discussed above
to re-train the model. The network will contain several hourglass modules. The
Hyperparameters will be specified which includes learning rate, number of epochs, loss
function,resize rato to name a few.

(5)EVALUATION: The trained model will be evaluated on the test data. I shall implement
this using pytorch library. Output two-channeled images from the model will be converted
into three-channeled images. F1 measure will be used to evaluae the performance of the
model.
