# Using Optuna for hyperparameter tuning
In this tutorial I will show an implementation of hyperparameter tunning in image classification using Optuna.

## Why Optuna
Neural Networks have usually many hyperparameters to tweak: the network architecture, the number of layers, the number of neurons per layer, the type of activation function...

One option is to simply try many combinations of hyperparameters and see which one gets better results. K-fold cross-validation, GridSearchCV and RandomSearchCV are a few examples of this strategy. They work by defining a list of hyperparameters and values to try, and build the final model using the best combination.

But this relies in a random search of the hyperparameters space, rather than focusing in the regions of the space that turned out to be good, like a 'zooming' process.

Optuna is an open source Hyperparameter optimization framework to automate hyperparameter search.

Directly from https://optuna.org:
    - Automated search for optimal hyperparameters using Python conditionals, loops, and syntax
    - Efficiently search large spaces and prune unpromising trials for faster results 
    - Parallelize hyperparameter searches over multiple threads or processes without modifying code 

## Loading the data
In this case we will use Fashion MNIST, a variation of MNIST. It has the exact same format as MNIST (70,000 grayscale images of 28 x 28 piexls each, with 10 classes), but it replaces the handwritten digits by fashion items.

![load_dataset](/images/Fashion-MNIST/load_dataset.svg "Loading dataset")

The dataset is composed by images like this:

![test_image](/images/Fashion-MNIST/test_image.png "Test Image")

## Implementing a Neural Network
As the images are in grayscale (single color channel), we must reshape them in this way: (N, height, size, 1). If the images were in RGB, the last number of the reshape sould be 3.

![load_dataset](/images/Fashion-MNIST/reshape_images.svg "Reshaping images")

### Optuna
The first hyperparameter to tune is the optimizer used during the model compilation. We pass 'Adam' and 'SGD' as options, each one with its learning rate (another hyperparameter) and, in the case of SGD, a momentum(also an hyperparameter).

![load_dataset](/images/Fashion-MNIST/create_optimizer.svg "Optimizers")

Next, we define the model in a function. It's a Sequential model, and we will tune the number of Conv2D and MaxPooling2D layers, in blocks, using a for loop. Also, the dropout rate used in the Dropout layers will be tuned.

![load_dataset](/images/Fashion-MNIST/build_model.svg "The model")

Finally, we define the function to minimize, including some parameters for the fit process and the hyperparameters: the number of blocks in the CNN, the dropout rate and the optimizer. Inside this function, the model is compiled and fitted with the train data, and also validated with validation data:

![load_dataset](/images/Fashion-MNIST/objective.svg "Compiling the model")

## Optimizing

And now, the process of optimization begins, during a number of trials defined in n_trials.

![load_dataset](/images/Fashion-MNIST/optimizing.svg "Optimizing")

Once finished, the best hyperparameters found can be accesed as:

![load_dataset](/images/Fashion-MNIST/best_params.svg "Best params")

and we can use them to create a new model that performs the best in the dataset:

![load_dataset](/images/Fashion-MNIST/best_model.svg "Best model")

Reducing the learning rate when a plateau is found is a useful technique to improve the model. It can be introduced in the CNN usign a keras callback:

![load_dataset](/images/Fashion-MNIST/reduce_lr.svg "Reduce Learning Rate")


The model is ready to compile and fit:

![load_dataset](/images/Fashion-MNIST/model.svg "Model")

The evolution of accuracies and losses with epochs is as follows:

![load_dataset](/images/Fashion-MNIST/accuracy_loss_evolution.png "Accuracy")

## Final comments
Optuna is just another tool for optimizing hyperparameters in Machine/Deep Learning models. Instead of using fixed values given by the user, Optuna zooms to regions of the hyperparameter space where the model got better results.

