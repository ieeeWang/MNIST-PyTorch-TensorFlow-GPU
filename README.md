# MNIST-PyTorch-TensorFlow-GPU

The [MNIST](http://yann.lecun.com/exdb/mnist/) dataset of handwritten digits for image classification using CNNs.

**Speed**  
Using my laptop with a GPU (Quadro M1200, Compute Capability = 5.0) to run the LeNet5, the speed of of two framworks as follow.

- TensorFlow: ~33s (10 epochs), see 'main_tf2x.ipynb' 
- PyTorch: ~92s (10 epochs), see 'main_pytorch.ipynb'


**Dataset**   
- For TensorFlow users, download is not needed, just load data in the code using TensorFlow built-in method.

- For Pytorch users, note that many old online/official examples have problems!
There has been trouble (e.g., 503 error) with the MNIST hosted on http://yann.lecun.com/exdb/mnist/ (by default if one uses torchvision.datasets.MNIST to download). Therefore pytorch got permission and hosting it now on amazon AWS.
For window users, it is much easier just go to www.di.ens.fr/~lelarge/MNIST.tar.gz, download it, and unzip the file. Then you will have MNIST folder, which you put into the root directory (e.g., ./data/) for dataloader.


**Dependencies**
- TensorFlow2.x
- PyTorch > 1.0
- Numpy


**References**   
- [A keras implementation for tensorflow](https://keras.io/examples/vision/mnist_convnet/)
- [The official pytorch MNIST Example](https://github.com/pytorch/examples/tree/master/mnist)
- [The pytorch tutorial on MNIST](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html#sphx-glr-beginner-blitz-neural-networks-tutorial-py)
- [LeNet5-paper](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf)
