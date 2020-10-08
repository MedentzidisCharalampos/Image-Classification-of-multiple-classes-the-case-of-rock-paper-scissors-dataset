# Image-Classification-of-multiple-classes-the-case-of-rock-paper-scissors-dataset
The dataset:

Consists of 3,000 images, all of the images have been generated using CGI with a diverse array of models, male and female and lots of different skin tones.   
The dataset can be found at this URL: http://www.laurencemoroney.com/rock-paper-scissors-dataset/. It will contain a training set and a validation set.

The Preprocessing of the dataset:

The training set:

1. The pixel values are rescaled in the [0, 1]
2. The images are:
  a. rotated by 40
  b. shifted  by 0.2 (the width and height seperately)
  d. sheared by 0.2
  e. zoomed by 0.2
  f. horizontal fliped
3. The dimesions rescaled (reduced) to 150 x 150
4. The batch size is: 126

The validation set:
1. The dimesions rescaled (reduced) to 150 x 150
2. The batch size is: 126








The architecture of the model:
The results:




