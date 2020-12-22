# Pokemon Classifying using a CNN
In this project I am going to try to design and train a CNN to classify different Pokemons from images. Due the few images available per class, I will use Image Augmentation to feed the CNN with more examples of each class/Pokemon.

## Image Augmentation
Suppose you want to train a CNN with images, but you don't have a large amount of them. Image Augmentation works by picking your images and rotating, scaling, flipping and zooming them, and adding this 'modified' images to your dataset. Hence, you end up with a larger set of images and, in some way, more different between them.

As an example, we choose this Pikachu image:

![Pikachu test](/images/pikachu_test_preview.png "Normal image")

and after applying the Image Augmentation operations, we obtain the following images:
![Pikachu augmentated](/images/preview_augmentated.png "Augmentated images")

## Dataset
The model will be trained using images from 7 different Pokemons/classes:
- Pikachu
- Mew
- Mewtwo
- Palkia
- Vulpix
- Kyogre
- Bulbasaur

The images were downloaded manually. I hope to find a way to automate the downloading process while maximizing the number of images available. Now, there are 100 images for training, 28 for validating and 7 for testing.

## Designing the model
I'll be using a CNN, with the following structure:
- Conv2D layer, 64 units, activation='relu', input_shape=(150, 150, 3).
- MaxPooling2D layer.
- Conv2D layer, 64 units, activation='relu', padding='same'.
- MaxPooling2D layer.
- Conv2D layer, 128 units, activation='relu', padding='same'.
- MaxPooling2D layer.
- Conv2D layer, 256 units, activation='relu', padding='same'.
- MaxPooling2D layer.
- Conv2D layer, 128 units, activation='relu', padding='same'.
- MaxPooling2D layer.

This is the output of model.summary():

Model: "sequential"

|Layer (type)   |  Output Shape     |  Param # |
|---------------|-------------------------------|-----------------|
|conv2d (Conv2D)|(None, 148, 148, 64) |1792   |   
|max_pooling2d (MaxPooling2D) |(None, 74, 74, 64)        |0|       
|conv2d_1 (Conv2D)            |(None, 74, 74, 64)        |36928|    
|max_pooling2d_1 (MaxPooling2D) |(None, 37, 37, 64)        |0|        
|conv2d_2 (Conv2D)            |(None, 37, 37, 128)       |73856|     
|max_pooling2d_2 (MaxPooling2D) |(None, 18, 18, 128)       |0|         
|conv2d_3 (Conv2D)            |(None, 18, 18, 256)       |295168    
|max_pooling2d_3 (MaxPooling2D) |(None, 9, 9, 256)         |0|         
|conv2d_4 (Conv2D)            |(None, 9, 9, 128)         |295040|   
|max_pooling2d_4 (MaxPooling2D) |(None, 4, 4, 128)         |0|         
|flatten (Flatten)            |(None, 2048)              |0|         
|dense (Dense)                |(None, 512)               |1049088|   
|dropout (Dropout)            |(None, 512)               |0|         
|dense_1 (Dense)              |(None, 7)                 |3591|      
=================================================================

Total params: 1,755,463

Trainable params: 1,755,463

Non-trainable params: 0
_________________________________________________________________

## Training the model
The model is trained locally on a GPU. As the number of images is very low, the number of epochs is fixed at 1000.

During the training, an accuracy is computed for both the train and validation data. Its evolution with the epochs can show whether the training process is long enough:

![Accuracy](/images/accuracy_plot.png)

## Get predictions
The model can be used now to predict the class of test images:

![Predicted images](/images/predicted_test.png)

6/8. Nearly perfect. The model correctly predicted all the Pokemon images, but it has not distinguished between Mew and Mewtwo, which is probably the main difficulty of this task given the large differences between the other classes, and the one with two Bulbasaurs.

Obviously, this is a simple project that could be harder to solve increasing the number of classes (Pokemons), or choosing more similar Pokemon, as in the mew/mewtwo example.
