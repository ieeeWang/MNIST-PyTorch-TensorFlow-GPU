# MNIST-PyTorch-TensorFlow-GPU
This repo uses the [MNIST](http://yann.lecun.com/exdb/mnist/) (handwritten digits for image classification) as an example to implement CNNs and to show the difference between two popular deeplearning framworks, PyTorch and TensorFlow.  

**Speed**  
Using my laptop with a GPU (Quadro M1200, Compute Capability = 5.0) to run the LeNet5 (~40k parameters, a CNN with two conv layers), the speed of using two framworks is as follow.

- TensorFlow: ~33s (10 epochs), see 'main_tf2x.ipynb' 
- PyTorch: ~92s (10 epochs), see 'main_pytorch.ipynb'


**Dataset**   
- For TensorFlow users, download is not needed, just load data in the code using TensorFlow built-in method.

- For Pytorch users, note that many old online/official examples have problems!
There has been trouble (e.g., 503 error) with the MNIST hosted on http://yann.lecun.com/exdb/mnist/ (by default if one uses torchvision.datasets.MNIST to download). Therefore pytorch got permission and hosting it now on amazon AWS.
For window users, it is much easier just go to www.di.ens.fr/~lelarge/MNIST.tar.gz, download it, and unzip the file. Then you will have MNIST folder, which you put into the root directory (e.g., ./data/) for dataloader.

- TensorFlow uses image dimension order (n, 28, 28, 1), whereas Pytorch uses (n, 1, 28, 28). Here 1 is the RGB channel number.


**Dependencies**
- TensorFlow2.x
- PyTorch > 1.0
- Numpy


**References**   
- [A keras-tensorflow implementation of CNN for MNIST](https://keras.io/examples/vision/mnist_convnet/)
- [An official pytorch MNIST Example](https://github.com/pytorch/examples/tree/master/mnist)
- [The official pytorch tutorial on MNIST](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html#sphx-glr-beginner-blitz-neural-networks-tutorial-py)
- [LeNet5-paper](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf)
