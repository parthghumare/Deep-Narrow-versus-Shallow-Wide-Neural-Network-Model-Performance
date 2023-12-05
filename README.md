# Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance
A study on why neural networks keep getting deeper but not wider for various industry applications.

The goal of this project is to compare the performance of deep and narrow versus shallow and wide neural networks on specific tasks to determine which architecture offers the best trade- off between accuracy, training time, and computational efficiency.

The world of neural networks presents an intricate panorama of architectures, methodologies, and applications. Neural networks are like the brains of artificial intelligence, designed to recognize patterns and make decisions based on data. They are divided into two main types: deep and shallow. While both are instrumental in tasks across machine learning domains, distinguishing between the two can unlock nuanced perspectives on their design principles and potential applicability.

## Primary Understanding of Deep and Narrow NN

Definition: A "deep" neural network
refers to a network that contains a
substantial number of layers. These
layers include hidden layers between
the input and output layers.

Neurons Per Layer: Despite the depth,
each layer has a relatively small
number of neurons, which defines the
'narrow' aspect. This contrasts with
wide networks that have many
neurons in each layer.

Layer Depth: These networks have a
significant number of layers, which is
characteristic of deep neural
networks. The depth allows for the
processing of data through multiple
levels of abstraction.

Parameter Count: Due to fewer neurons
per layer, these networks have a lower
number of parameters compared to
wide networks, which can lead to less
computational demand during training
and inference, and potentially faster
learning, albeit possibly at the expense
of the network's ability to capture more
complex patterns.

![image](https://github.com/parthghumare/Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance/assets/69133964/af907e33-66bc-4664-8e49-612d8fc13b25)


##Primary Understanding of Shallow and Wide NN

Definition: "shallow" neural network
refers to a network with a limited
number of layers, typically just one or
two hidden layers between the input
and output layers.

Parameter Count: With many neurons
in each layer, wide networks have a
high number of parameters, which
can lead to greater computational
demand during training and inference,
but can also allow for the capturing of
complex patterns without needing
deeper architectures.

Layer Depth: These networks have a
minimal number of layers, often just
the input layer, one or two hidden
layers, and the output layer.

Neurons Per Layer: In each of the few
layers, there is a high number of
neurons, which gives the network its
"wide" attribute.

![image](https://github.com/parthghumare/Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance/assets/69133964/8cff5b06-8c95-42d5-a42b-02944653bfd8)

##Model Design

Create two types of convolutional neural network (CNN) models and
then comparing two different architectures of neural networks, one
that is deep but narrow, and the other that is wider but shallower.
The key aspect of this comparison is to keep the total number of
trainable parameters approximately the same in both architectures.
This setup will allow us to explore whether the depth or width of a
network has a more significant impact on performance, given a
constant parameter budget.

• Deep and Narrow Network: This will have
many layers but fewer parameters per layer.

• Wide and Shallow Network: This will have
fewer layers but more parameters per layer.

##Data Source 1 - Image Classification

• The CIFAR-10 dataset consists of 60000 32x32 px color images in 10 classes, with 6000 images per class.
There are 50000 training images and 10000 test images.

• Source: https://www.cs.toronto.edu/~kriz/cifar.html

![image](https://github.com/parthghumare/Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance/assets/69133964/96cda9d0-6b63-423d-b69d-9531b656f303)

• We'll normalize the pixel values to be 0 to 1
by dividing by 255 (since pixel values range
from 0 to 255). For the labels, we'll use one-
hot encoding if necessary, depending on the
model requirements.



