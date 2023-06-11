# Learning_Activation_Function
## Introduction: 

Activation functions are crucial components in Artificial Neural Networks (ANNs), enabling them to model complex relationships and make accurate predictions. The choice of activation function greatly impacts the performance and convergence of ANNs. However, there is no universally optimal activation function for all datasets and tasks. Therefore, an adaptive activation function selection approach has been proposed to allow the network to autonomously determine the most suitable activation function based on the dataset. This report presents the implementation details of a 1-hidden layer neural network with adaptive activation function selection, aiming to showcase the importance of activation functions in ANNs and the potential benefits of adaptive selection.

Dataset used in this experiment - Bank-Note, Iris, Wisconsin Breast Cancer, MNIST 

## Initial Setting & Methodology: 

The methodology employed in this work involves the utilization of a 1-hidden layer neural network architecture for adaptive activation function (AF) selection. The main goal is to investigate the effectiveness of adaptively selecting the activation function in improving the network's performance in classifying samples from a dataset. The network architecture comprises an input layer, a hidden layer with the Ada_act custom layer, and an output layer. The Ada_act layer implements a flexible activation function using three parameters: k0, k1, and k2. These parameters are sampled from a distribution during the initialization process, allowing the network to explore different activation function configurations. The parameters k0, k1, and k2 are sampled from a distribution with specific ranges. 

For example, in this work, the parameters are sampled using the RandomUniform initializer, where k0 is randomly initialized between -0.01 and 0.1, k1 is initialized between -0.01 and 0.1, and k2 is initialized between 0.5 and 1.5. During the forward pass of the network, the Ada_act layer applies the activation function defined as k0 + k1 * x + k2 * x^2, where x represents the input values. This flexible functional form enables the network to capture the complex patterns present in the dataset and adapt its behavior accordingly. Through multiple runs of the neural network on the dataset, the parameters k0, k1, and k2 are updated based on the network's performance. 

This iterative process allows the network to converge to an optimal set of parameters, resulting in the selection of the most suitable activation function for the dataset. By incorporating the adaptive AF selection approach and utilizing the dataset, this methodology aims to demonstrate the effectiveness of adaptively selecting the activation function in improving the network's performance and its ability to accurately classify the samples. This approach provides insights into the potential of flexible activation functions for enhancing the performance of neural networks on various datasets.
