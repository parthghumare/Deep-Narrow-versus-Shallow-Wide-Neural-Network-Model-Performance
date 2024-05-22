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


## Primary Understanding of Shallow and Wide NN

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

## Model Design

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

## Data Source 1 - Image Classification

• The CIFAR-10 dataset consists of 60000 32x32 px color images in 10 classes, with 6000 images per class.
There are 50000 training images and 10000 test images.

• Source: https://www.cs.toronto.edu/~kriz/cifar.html

![image](https://github.com/parthghumare/Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance/assets/69133964/96cda9d0-6b63-423d-b69d-9531b656f303)

• We'll normalize the pixel values to be 0 to 1
by dividing by 255 (since pixel values range
from 0 to 255). For the labels, we'll use one-
hot encoding if necessary, depending on the
model requirements.

• We then train both neural networks and observe their performance.

## Data Source 2 - Binary Sentiment Classification

• The IMDB dataset which is a standard dataset used for binary sentiment classification. As of April 2023, this dataset contains 50,000 reviews split evenly into 25,000 reviews for training and 25,000 for testing. Each of these sets has an equal number of positive and negative reviews.

• Source: https://keras.io/api/datasets/imdb/

• The IMDB dataset in Keras is preprocessed for sentiment analysis. Each movie review is tokenized and encoded as a sequence of word indexes, represented as integers. Additionally, every review in the training dataset is labeled as either positive or negative.

• We then train both neural networks and observe their performance.

## Insights from Graphical Representations

![image](https://github.com/parthghumare/Deep-Narrow-versus-Shallow-Wide-Neural-Network-Model-Performance/assets/69133964/96cda9d0-6b63-423d-b69d-9531b656f303)

• We tested the performance of both types of neural network on two different datasets. One application was image recognition, and the other was NLP. In both the cases we saw that the deep and narrow model out-performed the shallow and wide model, despite having slightly a smaller number of parameters. This gives us an idea of how more layers in a neural network helps us better recognize the patterns in data and thus, has better generalization. On the other hand, more nodes and smaller number of layers lag in generalizing.

• In practice, the choice between a deep and narrow network versus a wide and shallow network is often a trade-off based on the specific requirements of the task, the nature of the input data, the availability of training data, and computational constraints. In some advanced architectures, a combination of both approaches is used to harness the strengths of each. For example, in some modern CNN architectures, there are initial layers that are wide and shallow to capture a broad range of features, followed by deeper layers to capture more abstract representations.

## Tips to choose between Deep and Narrow or Wide and Shallow model architecture

1. Assess Problem Complexity and Data Characteristics:
• Determine the complexity of your task. Use shallow networks for simpler problems and deep networks for more complex tasks involving hierarchical data structures.
• Analyze your data. Consider the volume and variety of features. Deep networks are typically more suited for large and complex datasets.
2. Evaluate Computational Resources and Performance Needs:
• Consider the available computational power and memory. Deep networks require more resources.
• Identify the performance and accuracy requirements of your task. Deep networks often provide higher accuracy for complex tasks, but shallow networks are more efficient and faster to train (But not always).
3. Risk of Overfitting and Model Interpretability:
• Assess the risk of overfitting, especially if you have a limited amount of data. Shallow networks are less prone to overfitting.
• If you need a more interpretable model, shallow networks are generally easier to analyze and understand.
4. Experiment and Validate:
• Conduct experiments with both architectures to compare their performance on your specific task.
• Use validation techniques to evaluate the models and refine your choice based on results.








