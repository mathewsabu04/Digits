
# Training a neural network to recognize handwritten digits.

The MNIST dataset is a standard benchmarking dataset for computer vision algorithms.  Each item in the dataset is a
28x28-pixel grayscale image of a handwritten decimal digit, and comes with a human-produced label identifying which
digit (0-9) is depicted in the image.

Supervised learning algorithms can be used to train a model, using the labeled data, to recognize digits in new images.

In this assignment, you will produce an implementation of multilayer neural networks and then train and evaluate the 
performance of a neural network on the MNIST dataset.

### Installing this project

- If you use terminal to run the program
    - From within this project, run `python3 -m venv .venv` to create a new python environment.
    - Activate the python environment by running `source .venv/bin/activate`
    - Install required packages in the python environment by running `pip install -r requirements.txt`
- If you use Pycharm, you can just open the folder and click "OK" when it asks you if you would like to create
A virtual environment using it

### What's in the project?

- The `data` folder contains files containing the dataset.  There are 60,000 training images and 10,000 test images.
- `loader.py` contains a utility class for loading all the training and test images, as well as their labels, from the
                   data files
- `try_loader.py` is a script you can run to make sure your env is installed and the data loader is working properly.
- `train_model.py` is a script that will create a new model, train it using the training data,
                and save the trained model on disk in `mnist_ann.pickle`.
- `test_model.py` is a script that will load the model saved in `mnist_ann.pickle`, apply it to each example in the
                   test dataset, and tell you how many examples out of 10,000 it got wrong.
- `ann.py` is the file where you will do most of your work.  There is a stubbed out `NeuralNetwork` class which is
         used by both the training script and the test script.  You must implement its methods in order to satisfy
         the contract assumed by those two scripts.  If you do it properly, then your trained model will be able to
         recognize most handwritten digits correctly, getting maybe a few hundred out of the 10,000 test examples wrong.

### Looking at some of the dataset

With the project's python environment activated, run `python -m learn_mnist.try_loader`.

It will load the data set and display a random selection of images with their labels, from both the training set and
the test set.

(If you use pycharm, run try_loader.py. If there is a problem with pycharm running it from the wrong folder, then you
can update the run configuration to use the correct working directory)

You are able to do this before you write any code for the assignment.

### Training your model

With the project's python environment activated, run `python -m learn_mnist.train_model`.

The script will take some time to run, but you can watch its progress in your terminal.  When it is done, it will
have saved the trained neural net in the `mnist_ann.pickle` file. 
This overwrites anything that is currently in the file, so if you are trying to keep around multiple trained models
you might want to copy the file before running this file a second time.

It should go without saying that you must add the necessary logic to `ann.py` before this script will work.

As you iterate on you neural network logic and try to get it correct, you may want to use this file to exercise your code.
But if you do, you might do best to reduce the number of training epochs so that it does not take so long to run.

(Again, If you use pycharm, run train_model.py. If there is a problem with pycharm running it from the wrong folder, then you
can update the run configuration to use the correct working directory)

### Testing your model

With the project's python environment activated, run `python -m learn_mnist.test_model`.

It will apply the trained model from the `mnist_ann.pickle` file to all 10,000 test examples and check the output
against the real label.

Watch the terminal output to see how it does.

(Again, If you use pycharm, run test_model.py. If there is a problem with pycharm running it from the wrong folder, then you
can update the run configuration to use the correct working directory)

If the error rate is low, it indicates that you are successful for doing the project. 
You can stop at this point, however, if you want to play around, you can do the following.

### Play around

The training script prescribes a specific network topology, using a sigmoid activation function for every neuron.
A model following this specification does OK at the MNIST classification task.  But maybe you can do better!

Try whatever you like: more layers, different activation functions, wider layers, narrower layers, etc.

Have fun!# Digits
# Digits
