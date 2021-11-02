# Phone-Locator

Find location of a phone placed on the floor in a single RGB camera image. Use any pretrained neural networks available online or build a simple convolution nural network to predict the center coordinates of the phone. Use any DL frameworks/libraries of you choice (Tensorflow, Keras, PyTorch, etc.)

# Dataset
Dataset contains 129 rgb images of size 490 x 326 and the labels are in the labels.txt file. Each line in the labels.txt contains image path, x center coordinate, y center coordinate: img_path , x , y

Example of an image from the dataset is shown below:

<br /> <br />
<img src="find_phone/0.jpg">
<br /> <br />
Top-left corner of the image
is defined as (x, y) = (0, 0), bottom-left as (x, y) = (0, 1), top-right as (x, y) = (1, 0), and finally
bottom-right corner as (x, y) = (1, 1). Goal is to find normalized coordinates
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
 


