#Neural_Network_Traffic (CS50AI)

An AI to identify which traffic sign appears in a photograph.

Please visit the [Following Link](https://cs50.harvard.edu/ai/2020/projects/5/traffic/) for more information about the project.

These are the following observations that I noticed after running Neural Network models for over a hundred times for this project.

### Convolutional Layers

Convolutional Layers are pretty important for Neural Network models since these Convolutional Layers draw out different feature maps that help in improving the accuracy of a model. For this project, the more the number of different Convolutional Layers, the better was the accuracy of the model. The only drawback of adding more Convolutional Layers is the increased computation time in training the model. Also after a few different Convolutional Layers the accuracy of the model didn't change much upon adding further Convolutional Layers. The size of kernels used in Convolutional Layers also matter in determining the accuracy of a model. For this project, ( 2 * 2 ) kernel performed worse than ( 3 * 3 ) or ( 4 * 4 ) kernels. As the size of kernels increased over a specific value ( kernel size > ( 4 * 4 ) ) the accuracy of the model also decreased along the way. The more the number of filters on a specific sized kernel, the more was the computation time but the accuracy of the model remained more or less the same expect when the number of filters were very high ( number of filters > 100 ) in which case accuracy of the model got worse in some cases.

### Pooling Layers

Adding different Pooling Layers reduces the computation time for a model but it also comes with a slightly reduced accuracy of the model since the image after pooling might be a better representation of the original with fewer pixels but it's still a pooled image and not the original. As the Pooling size of a Pooling Layer increases, the computation time decreases and also accuracy decreases slightly.

### Hidden Layers

The number and sizes of Hidden Layers depend on the problem we're trying to model our Neural Network for. For this project, One hidden layer was enough to get to an accuracy of over 97% consistently but what truly matters are the number of neurons in the hidden layer. If the number of neurons in a hidden layer is too low (< 200 (for this project)) the accuracy of the Neural Network got much worse. Also, far too many neurons in a hidden layer wouldn't increase the accuracy too much, after a specific value (around 1000 neurons for this project) the accuracy didn't change much at all and only computation time increased upon increasing the number of neurons over 1000.

### Dropouts

Dropouts in a Neural Network usually decrease the accuracy of a model slightly. Dropouts effects are more visible when the number of neurons in the hidden layers gets too low ( around 200 for this project ) in which case accuracy gets much worse for a model.

  





