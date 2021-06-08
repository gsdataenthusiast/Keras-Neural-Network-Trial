# Keras-Neural-Network-Trial - Output Analysis
Artificial Neural Network for 4- class classification problem:

To build an artificial neural network that classifies the input into four different classes, the linear stack of layers was constructed using sequential model. I tried few different models with combination of hidden layers to find an optimal model with reasonable number of layers.

The input_shape was defaulted to 2, implying that our input layer has 2 nodes. The output layer was also defaulted to a fully connected dense layer with 4 nodes representing 4 classes with ‘SoftMax’ activation. The SoftMax activation normalizes the output of the network into a probability distribution over the 4 classes.

Optimal Model:

The model was constructed with a total of layers stacked linearly as below,

![image](https://user-images.githubusercontent.com/68840596/121188018-cafe4380-c8bc-11eb-998f-794ae15b906f.png)

As said earlier, the input to the first dense layer was 2 followed by 4 hidden layers with decreasing number of nodes per each layer as 128, 64, 32 and 16. The hidden layers are ‘dense’ layer implying that each layer is fully connected to each other. The activation function used to activate the neurons is ‘tanh’ or hyperbolic tangent activation function so that the outputs of the neurons will range over (-1,1). All the parameters are trained making the count of trainable parameters to 11,316. 

The loss function used is categorical cross entropy since this is a multi – class problem. Adam optimizer is used to decrease the loss function.

Model Performance:

The model was trained with 50 epochs as given and the loss/accuracy graph was plotted to visualize the model performance over epochs.

![image](https://user-images.githubusercontent.com/68840596/121188149-ed905c80-c8bc-11eb-9a7c-2912f8880e59.png)





 
                          Fig: Loss and Accuracy over the training period



As we can see, both the loss and accuracy curve of the model is good. The model has been trained well within 10 epochs and retained similar performance throughout the training period with minor fluctuations in the middle. The loss was around 0.132 and accuracy was around 0.95. Let us further discuss the performance of the model with the classification report.

![image](https://user-images.githubusercontent.com/68840596/121188243-08fb6780-c8bd-11eb-8265-1420750fbcf3.png)


 
                         Fig: Classification Report


All the metrics like precision, recall, f1- score, accuracy are above 90% indicating the overall goodness of the model. The precision for class 1 and 2 is 100% indicating that all are correctly classified in those classes. Since the classes are equally available for training these metrics will be ideal indicator of the overall performance of the model.





The classification can also be visualized using decision boundary as below,

![image](https://user-images.githubusercontent.com/68840596/121188274-11ec3900-c8bd-11eb-9dcc-013c51f43acf.png)

 
                       Fig: Non-Linear Decision Boundary for 4 classes.


The decision boundary shows how each class is distinctly classified with very few misclassified data points.

Conclusion:

It was noted from other trials that even a model with 2 hidden layers produced more than 90% accuracy. The models with 3 hidden layers given almost similar results as above but this deep learning model with 4 hidden layers will generalize better with a reasonable model size and efficiency for the given number of epochs and act as a powerful model for this multi-class classification problem.
