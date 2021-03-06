# SimpNet-Tensorflow

<p align="center">
    <img src="http://uupload.ir/files/1b38_image-2018-09-01.png">
</p>

---

By [Ali Gholami](https://hexpheus.github.io),
Bio-intelligence Research Unit, [Sharif University of Technology](http://www.en.sharif.edu/).

### Introduction

This repository contains the first unofficial implementation of SimpNet architecture described in the paper "
Towards Principled Design of Deep Convolutional Networks: Introducing SimpNet" (https://arxiv.org/abs/1802.06205).

### Todo

- [x] Xavier weight initialization for layers {1, 2, 6, 7, 8, 9, 10, 11, 12, 13}
- [x] Gaussian weight initialization for layers {3, 4, 5}
- [ ] Feed flipped images
- [x] Shuffle input data
- [ ] Adaptive learning rate for the Adam
- [ ] Moving average on the batch norms (M.A. Fraction = 0.95)
- [x] Fix SafPool dropout rates
- [ ] Multi-label accuracy reports
- [ ] LOSS = 1 - ACC
- [ ] Learning Rate Visualization
- [x] AdaDelta Optimizer
- [x] Convolution Strides Optimization
- [x] Multilabel Confusion Matrix

### Installation

The instructions are tested on Ubuntu 16.04 with python 3.6 and tensorflow 1.10.0 with GPU support. 
- Clone the SimpNet	 repository:
    ```Shell
    git clone https://github.com/hexpheus/SimpNet-Tensorflow.git
    ```

- Setup virtual environment:
    1. By default we use Python 3.6. Create the virtual environment
        ```Shell
        virtualenv env
        ```

    2. Activate the virtual environment
        ```Shell
        source env/bin/activate
        ```

- Use pip to install required Python packages:
    ```Shell
    pip install -r requirements.txt
    ```

### Visualization

- We can monitor the training process using tensorboard.
    ```Shell
    tensorboard --logdir graphs/simpnet/
    ```
    Tensorboard displays information such as training loss, evaluation accuracy, visualization of detection results in the training process, which are helpful for debugging and tunning models, as shown below:

### MNIST Performance

Here is the **loss** and **accuracy** results after running the model on the MNIST dataset. Results shown here are provided after 18 epochs of training. **Note** that the accuracy provided here is based on the number of true predictions in each batch. Batch size is 140 in the following training.

#### Accuracy

<p align="center">
    <img src="https://github.com/hexpheus/SimpNet-Tensorflow/blob/master/result/mnist_acc.png">
</p>

---

#### Loss
<p align="center">
    <img src="https://github.com/hexpheus/SimpNet-Tensorflow/blob/master/result/mnist_loss.png">
</p>

### Citation

If you use these models in your research, please cite:

	@article{hasanpour2018towards,
	  title={Towards Principled Design of Deep Convolutional Networks: Introducing SimpNet},
	  author={Hasanpour, Seyyed Hossein and Rouhani, Mohammad and Fayyaz, Mohsen and Sabokrou, Mohammad and Adeli, Ehsan},
	  journal={arXiv preprint arXiv:1802.06205},
	  year={2018}
	}

### Official Implementation
You can find the official implementation [here](https://github.com/Coderx7/SimpNet).

### Important Note
This model has yielded stunning results on both MNIST and Fashion MNIST datasets. Other datasets should be tested for evaluation.

