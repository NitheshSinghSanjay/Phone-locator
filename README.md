# Phone-Locator

Find location of a phone placed on the floor in a single RGB camera image. Use any pretrained neural networks available online or build a simple convolution neural network to predict the center coordinates of the phone. Use any DL frameworks/libraries of you choice (Tensorflow, Keras, PyTorch, etc.)

# Dataset
Dataset(/find_phone) contains 129 rgb images of size 490 x 326 and the labels are in the labels.txt file. Each line in the labels.txt contains image path, x center coordinate, y center coordinate: img_path , x , y

Example of an image from the dataset is shown below:

<br /> <br />
<img src="find_phone/0.jpg">
<br /> <br />
Top-left corner of the image
is defined as (x, y) = (0, 0), bottom-left as (x, y) = (0, 1), top-right as (x, y) = (1, 0), and finally
bottom-right corner as (x, y) = (1, 1). Goal is to find normalized center coordinates
of the phone. In the example above, the coordinates of the phone are
approximately (x, y) = (0.83, 0.13).


# Requirements
Project folder should have a dataset folder, train.py, infer.py & README.md. Create any aditional files if required.

1. train.py 
   * Should take the "dataset path" as a command line argument (Eg. `$ python train.py <dataset-path>`)
   * Function(s) to Build & Load the Neural Network, Load the training data, Train, Save the trained model
   * Save the best trained model in the project folder
   
2. infer.py
    * Should take "image path" as a command line argument (Eg. `$ python infer.py <image-path>`)
    * Function(s) to load a trained model, load an image, predict location, print results (location coordinates)

3. README.md
    * Describe the neural network, optimizer, loss function used in solving the problem.
    * Performance metrics (Final accuracy, loss, etc)
    * Instructions to run the code



