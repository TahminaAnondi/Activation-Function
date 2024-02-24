# Activation-Function
Activation function decides whether a neuron should be activated or not by calculating the weighted sum and further added bias to it. Activation function fires if the input is big enough, otherwise nothing happens. 

Real Life Example:Suppose we are trying to decide whether to be excited or not based on how much we’ve accomplished during the day. So here,  

Input = Our accomplishments of the day (for example finishing homework or exercise etc.) 

Processing = your brain(neural network) takes these accomplishments and process them. 

Activation function = This is like our mood threshold. If our accomplishments exceed a certain level(let’s say we finished all my task), we’ll be excited. If not, we’ll be neutral or maybe a little bit down. 

Output = Our mood(excited/neutral/down).  
 

![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/9cfabc33-6be2-4634-87b4-10313c5977d7)


The four most activation functions in deep learning are: 

Sigmoid Function (Logistic Function): The sigmoid function, also known as the logistic function) maps the incoming input between 0 and 1. The graph of a sigmoid function is characterized by its S-shaped curve or “sigmoid curve”. 
![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/ec1d9196-c224-4009-bd61-c1c5b743a7ce)

This function is commonly used in machine learning because they help neural networks understand and learn from complex patterns in data. They introduce non-linearity to the data, which means the relationship between input and output is not a simple straight line. Instead, sigmoid activation functions can help neural networks capture intricate and non-linear relationships. This is important because problems that are encountered in the real-world, such as image recognition or language processing, often have behaviors that are not straightforward or linear. Sigmoid activation functions allow the neural network to handle these complexities. 

 Practical uses for sigmoid activation function: 

Binary classification: Sigmoid activation functions are especially useful in binary classification tasks, where samples are assigned to one of two classes. In such tasks, a threshold (typically 0.5) can be set so that values above the threshold are classified into one class, and values below the threshold are classified into the other class. 

Sentiment analysis: Sentiment analysis aims to determine the emotion, or sentiment, of text data. Sigmoid activation functions can be used to assign probabilities to different sentiment classes, such as positive or negative sentiment. 

Fraud detection: Sigmoid activation functions can be used in neural networks to detect the likelihood of a transaction being fraudulent based on multiple transaction features. 

Financial risk assessment: Sigmoid activation functions can be used in neural networks to assign probabilities to different risk factors, such as credit risk or the likelihood of loan defaults. 

Limitations: 

Vanishing Gradient: Sigmoid functions can suffer from the vanishing gradient problem, especially in deep neural networks. This occurs when gradients become extremely small during backpropagation, hindering the training process. 

Biased Outputs: Sigmoid outputs tend to be biased towards extreme values (0 or 1) when the input is far from zero. This can slow down learning, especially in the hidden layers of neural networks. 

 

Tanh Activation Function: Historically, the tanh function became preferred over the sigmoid function as it gave better performance for multi-layer neural networks. But it did not solve the vanishing gradient problem that sigmoids suffered, which was tackled more effectively with the introduction of ReLU activations. 
![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/738226c3-1690-44cf-847a-ad1a55d8034c)

 

Practical uses for sigmoid activation function: 

Hidden Layers: Tanh activation functions are commonly used in the hidden layers of neural networks. They help introduce non-linearity to the model and enable the network to learn complex patterns in the data. 

Recurrent Neural Networks (RNNs): Tanh activation functions are often used in RNNs due to their zero-centered nature, which helps alleviate the vanishing gradient problem commonly encountered in these architectures. 

Limitations: 

Vanishing Gradient: While tanh addresses some of the issues with the sigmoid function, it can still suffer from the vanishing gradient problem, particularly in deep neural networks with many layers. 

Saturation: The tanh function saturates at extreme values (-1 or 1), which can lead to slower learning in certain cases. 

Rectified Linear Unit (Relu):  

ReLU stands for rectified linear unit, and is a type of activation function. Mathematically, it is defined as y = max(0, x). Visually, it looks like the following: 

 ![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/522c18bd-1aaa-4907-bab1-96e5dc4069e4)


ReLU is the most commonly used activation function in neural networks, especially in CNNs. 

Practical uses for sigmoid activation function: 

Hidden Layers: ReLU is commonly used as the activation function in the hidden layers of neural networks. It has been shown to perform well in practice, facilitating faster convergence during training compared to traditional activation functions like sigmoid and tanh. 

Convolutional Neural Networks (CNNs): ReLU is particularly popular in CNNs for image classification tasks. Its simplicity and ability to learn sparse representations make it well-suited for processing high-dimensional data like images. 

Deep Learning: ReLU has been instrumental in the success of deep learning models, enabling the training of very deep neural networks with many layers. 

Limitations: 

Dying ReLU: A common issue with ReLU is the problem of "dying" ReLU units, where neurons can become stuck in a state where they output zero for all inputs. This usually happens when the weights associated with a neuron are adjusted such that it never activates (i.e., always outputs zero) during training. 

Unbounded Activation: Unlike sigmoid and tanh, ReLU does not have an upper bound, which can lead to exploding activations in certain scenarios. This may require careful initialization and regularization techniques to mitigate. 

 

Leaky Relu: A problem we see in ReLU is the Dying ReLU problem where some ReLU Neurons essentially die for all inputs and remain inactive no matter what input is supplied, here no gradient flows and if large number of dead neurons are there in a Neural Network it’s performance is affected, this can be corrected by making use of what is called Leaky ReLU where slope is changed left of x=0 in above figure and thus causing a leak and extending the range of ReLU. 

 ![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/572cac5d-392b-4e08-8cbf-2c6d03a90663)


With Leaky ReLU there is a small negative slope, so instead of not firing at all for large gradients, our neurons do output some value and that makes our layer much more optimized too. 
![image](https://github.com/TahminaAnondi/Activation-Function/assets/68536783/a1c1963b-cccf-40f8-9308-62001d6c2185)

where .01 is a small constant called the leak coefficient. 

Practical uses for sigmoid activation function: 

Hidden Layers: Leaky ReLU is often used as the activation function in the hidden layers of neural networks, particularly in scenarios where "dying ReLU" is observed during training. 

Deep Learning: In deep neural networks with many layers, Leaky ReLU can be beneficial for preventing the vanishing gradient problem associated with traditional activation functions like sigmoid and tanh. 

Limitations: 

Additional Parameter: Introducing the leak coefficient α(.01) adds an additional parameter to the model that needs to be tuned during training. 

Choice of α(.01): The choice of the leak coefficient α(.01) is important and requires careful consideration. Setting it too high may lead to a loss of representational capacity, while setting it too low may not effectively prevent the "dying ReLU" problem. 

References: 

1.https://himanshuxd.medium.com/activation-functions-sigmoid-relu-leaky-relu-and-softmax-basics-for-neural-networks-and-deep-8d9c70eed91e 

2.https://www.javatpoint.com/activation-functions-in-neural-networks#:~:text=Equation%3A%20A%20linear%20function's%20equation,are%20all%20linear%20in%20nature. 

3. https://www.geeksforgeeks.org/activation-functions-neural-networks/ 

4.https://artemoppermann.com/activation-functions-in-deep-learning-sigmoid-tanh-relu/ 

5. https://en.wikipedia.org/wiki/Activation_function 
