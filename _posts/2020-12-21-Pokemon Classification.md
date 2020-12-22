# Pokemon Classifying using a CNN
In this project I am going to try to design and train a CNN to classify different Pokemons from images. Due the few images available per class, I will use Image Augmentation to feed the CNN with more examples of each class/Pokemon.

## Image Augmentation
Suppose you want to train a CNN with images, but you don't have a large amount of them. Image Augmentation works by picking your images and rotating, scaling, flipping and zooming them, and adding this 'modified' images to your dataset. Hence, you end up with a larger set of images and, in some way, more different between them.

![Image Augmentated](/images/pokemon_class/image_augmentated.svg "Image Augmentated")

As an example, we choose this Pikachu image:

![Pikachu test](/images/pokemon_class/pikachu_test_preview.png "Normal image")

and after applying the Image Augmentation operations, we obtain the following images:
![Pikachu augmentated](/images/pokemon_class/preview_augmentated.png "Augmentated images")

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
![Model design](/images/pokemon_class/model_design.svg "Model design")

This is the output of model.summary():

![model_summary](/images/pokemon_class/model_summary.svg "Model summary")

## Training the model
The model is trained locally on a GPU. As the number of images is very low, the number of epochs is fixed at 1000.

During the training, an accuracy is computed for both the train and validation data. Its evolution with the epochs can show whether the training process is long enough:

![Accuracy](/images/pokemon_class/accuracy_plot.png)

## Get predictions
The model can be used now to predict the class of test images:

![Predicted images](/images/pokemon_class/predicted_test.png)

6/8. Nearly perfect. The model correctly predicted all the Pokemon images, but it has not distinguished between Mew and Mewtwo, which is probably the main difficulty of this task given the large differences between the other classes, and the one with two Bulbasaurs.

Obviously, this is a simple project that could be harder to solve increasing the number of classes (Pokemons), or choosing more similar Pokemon, as in the mew/mewtwo example.
