# WeatherID
This is the final project I carried for the ENEL 525 Machine Learning for Engineers course at the University of Calgary. 

This project consists on the building and training of a convolutional neural network to identify the weather of different images. In this case, it is able to determine whether a picture contains a sunshine, rainy, cloudy or sunrise environment. The images used for training are available at the "Multi-class Weather Dataset for Image Classification" by Gbeminiyi Ajayi with DOI, 10.17632/4drtyfjtfy.1 available at https://data.mendeley.com/datasets/4drtyfjtfy/1 . There are two methods of preprocessing, reason why there are two different Jupyter files. In the first one, the images are cropped in the upper left corner by the smaller image size so all images are included in the training. In the second one, the function reshape is utilized as to include all images once again. The selection of which images to utilize in the training is given by the variable `randomizer`. If you want to randomize which images are selected, set this to True and change the variable `percentage` to the portion of images that you want be used in training. In this case it is set to 80%. 

# Usage
To utilize this code you will need to download the previously mentioned set of images in your computer and change the `path` variable to the folder where the images are located. This code is more manual in the sense you need to manually add the path where each class of images are located in order to train them. If you want to use less images for clouds so the same number of images for each class are used to train the model, change the variable clouds in the first cell to the desired number and set `randomizer` to True, so random images are selected in the training. You can add more images of your own, but be sure to name them correctly and change the variable number in the first cell. 

# Improvements
The following improvements can be made to the program: 

- [ ] Generalize the program so more classes can be added by just changing a variable. 
- [ ] Reduce manual intervention in the program. For example, folders containing the number of images. If more classes are to be added, the definition of `train_data` defined in cell 9 must be generalized too.
- [ ] A better pre-processing of images. Now, the reshape function and upper left corner cutting were used, but since these are sky images, working with upper centered sections could work best. 
- [ ] Try with different activation functions and architectures. Adapting the kernel size through the process to capture details better can perform more optimally and also changing the activation function to softmax for the final layer.
- [x] Explore the option of using reshape and resize functions instead of cropping the images.
