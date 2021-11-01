# Phone-Locator

# Problem Description

This project goal is to find location of a phone dropped on the floor from a single RGB
camera image. This is a regression problem which can be solved using a simple convolution nural network. Example of the image is shown below:


<br /> <br />
<img src="find_phone/0.jpg">
<br /> <br />
Left-top corner of the image
is defined as (x, y) = (0, 0), left-bottom as (x, y) = (0, 1), right-top as (x, y) = (1, 0), and finally
right-bottom corner as (x, y) = (1, 1). Goal is to find normalized coordinates
of the center of the phone. In the example above, the coordinates of the phone are
approximately (x, y) = (0.83, 0.13).


1. train.py 
    * train.py should take the "dataset path" as a command line argument (Eg. python train.py <dataset-path>)
    * Use any DL libraries such as tensorflow, keras, pytorch to build a neural network to solve the problem
    * Build & Load the Neural Network -> Load the training data -> Train -> Save the trained model 
    * Training function should also log data during training (eg: epoch number, train acc, val acc, loss etc)
    * Save the trained model in the root dir of the project
2. infer.py
    * infer.py should take "image path" as a command line argument (Eg. python infer.py <image-path>)
    * Load the trained model -> Load the image -> predict location -> print result(location coordinate)
 

# Dataset
Dataset contains 129 rgb images of size 490 x 326 x 3 and the labels are in the labels.txt file. Each line of the labels.txt is composed of img_path , x , y separated by spaces: <br />
img_path , x (coordinate of the phone), y (coordinate of the phone)
