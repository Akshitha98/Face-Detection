# Face-Detection

This is a simple python program which uses OpenCV and Haar Cascade classfiers to detect a face. 

**Haar Cascade**
Haar feature-based cascade classifiers is an effective object detection method proposed by Paul Viola and Michael Jones. It is a machine learning approach where a cascade function is trained from a lot of positive and negative images. It is used to detect objects in other images.   
Haar features include Edge Features, Line Features and Four-rectangle Features. Each feature is a single value obtained by subtracting sum of pixels under the white rectangle from sum of pixels under the black rectangle.
![Alt text](https://docs.opencv.org/3.4.1/haar_features.jpg)  
To find the face region in the given image, lot of time is taken. For this they introduced concept of Cascade of CLassifiers. In this,the features are grouped into different stages of classifiers and applied one-by-one. (Normally the first few stages will contain very many fewer features). If a window fails the first stage, discard it. We don't consider the remaining features on it. If it passes, apply the second stage of features and continue the process. The window which passes all stages is a face region.

**Haar-cascade Detection in OpenCV**   
OpenCV comes with a trainer as well as detector. Here we will deal with detection. OpenCV already contains many pre-trained classifiers for face, eyes, smiles, etc. Those XML files are stored in the opencv/data/haarcascades/ folder. We create a face and eye detector with OpenCV.

In this program, we capture the live video as an image, apply the classifiers on that live image captured and detect the face if any. The live image capture can be done using OpenCV functions. We load the required XML classifiers then take in the live captured image as input in gray scale mode. The result or output is an image with a blue square drawn over a face and green square drawn over the eyes.
