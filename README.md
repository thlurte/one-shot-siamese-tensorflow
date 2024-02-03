 <h2 align="center">Siamese Neural Networks</h2>
tensorflow implementation of (Koch et al. 2015)
<br>

<p align="center">
  <img src="assets/a.png" alt="Siamese Neural Network Architecture">
</p>


### Instructions

- Set Up Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate 
```

- Clone the repository
```bash
git clone https://github.com/thlurte/SiameseNet-tensorflow.git

```

- Change into the directory of the repository

```bash

cd SiameseNet-tensorflow
```

- Install Dependancies

```bash
pip install -r requirements.txt
```

- To Train the model

```bash
python main.py --data_dir <path-to-dataset>

```


###  Architecture

The model consists of a sequence of convolutional layers, each of which uses a single channel with filters of varying size and a fixed stride of 1.



### Activation 

The network applies a ReLU activation function to the output feature maps, optionally followed by maxpooling with a fliter size and stride of 2. 

### Loss Function
Binary Cross Entropy is used as loss function to calculate the error.

### Optimizer
Adam is used to find the global minima in this architecture.

### Weight Initialization
All network weights are initialized in the convolutional layers from a normal distribution with zero-mean and a standard deviation of $10^{−2}$. Biases were also initialized from a normal distribution, but with mean 0.5 and standard deviation $10^{−2}$.

  

### References

- [Siamese-Neural-Networks-for-One-shot-Image-Recognition](https://github.com/nevoit/Siamese-Neural-Networks-for-One-shot-Image-Recognition)
- [Siamese neural networks for one-shot image recognition](https://paperswithcode.com/paper/siamese-neural-networks-for-one-shot-image)
