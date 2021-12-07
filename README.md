# DCGAN
With recent advances in deep learning, machine learning algorithms have evolved to such an extent that they can compete and even defeat humans in some tasks, such as image classification on ImageNet [1], playing Go and Texas Hold’em poker. However, we still cannot conclude that those algorithms have true “intelligence”, since knowing how to do something does not necessarily mean understanding something, and it is critical for a truly intelligent agent to understand its tasks.
In the case of machine learning, we can say that, for machines to understand their input data, they need to learn to create the data. The most promising approach is to use generative models that learn to discover the essence of data and find a best distribution to represent it. Also, with a learned generative model, we can even draw samples which are not in the training set but follow the same distribution.
As a new framework of generative model, Generative Adversarial Net (GAN) , proposed in 2014, is able to generate better synthetic images than previous generative models, and since then it has become one of the most popular research areas. A Generative Adversarial Net consists of two neural networks, a generator and a discriminator, where the generator tries to produce realistic samples that fool the discriminator, while the discriminator tries to distinguish real samples from generated ones.
## An Overview of GAN
A generative adversarial network (GAN) has two parts:
The generator learns to generate plausible data. The generated instances become negative training examples for the discriminator.
The discriminator learns to distinguish the generator's fake data from real data. The discriminator penalizes the generator for producing implausible results.
When training begins, the generator produces obviously fake data, and the discriminator quickly learns to tell that it's fake. As training progresses, the generator gets closer to producing output that can fool the discriminator. Finally, if generator training goes well, the discriminator gets worse at telling the difference between real and fake. It starts to classify fake data as real, and its accuracy decreases.<br>
Here's a picture of the whole system:<br>
![](https://github.com/TheCoolNerd27/DCGAN/blob/main/GAN.png)
Both the generator and the discriminator are neural networks. The generator output is connected directly to the discriminator input. Through backpropagation, the discriminator's classification provides a signal that the generator uses to update its weights.
Now that we have a basic knowledge of how GAN functions, we tried it on some classic datasets
## MNIST Handwritten Digit Dataset
The MNIST dataset is an acronym that stands for the Modified National Institute of Standards and Technology dataset.
It is a dataset of 70,000 small square 28×28 pixel grayscale images of handwritten single digits between 0 and 9.
The task is to classify a given image of a handwritten digit into one of 10 classes representing integer values from 0 to 9, inclusively.
Keras provides access to the MNIST dataset via the mnist.load_dataset() function. It returns two tuples, one with the input and output elements for the standard training dataset, and another with the input and output elements for the standard test dataset.
## Fashion MNIST 
The Fashion MNIST dataset that is publicly available at the TensorFlow website. It consists of a training set of 60,000 example images and a test set of 10,000 example images. Each image in the
dataset has the size 28 x 28 pixels. Each training and test image belongs to one of the classes including T_shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, and Ankle boot.
## Large-scale CelebFaces Attributes (celebA) dataset
CelebFaces Attributes Dataset (CelebA) is a large-scale face attributes dataset with more than 200K celebrity images, each with 40 attribute annotations.
