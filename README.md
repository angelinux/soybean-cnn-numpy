# soybean-cnn-numpy

This is a simple multiclass classifier based on a Convolutional Neural Network (CNN) written only with numpy.

## Dataset

The dataset used in this notebook is the [weed detection in soybean crops](https://www.kaggle.com/fpeccia/weed-detection-in-soybean-crops) taken from Kaggle.

With the help of OpenCV, the original dataset was resized to a smaller size and reduced to its grayscale version, to reduce training time.

For example a typical image is [![soybean original](figs/soybean.png)]() and it is converted to [![soybean converted](figs/soybean2.png)]() before the training.


## Notebook

This jupyter notebook defines every single component of a CNN:

1. a convolutional layer that applies a filter to an image [![convolutional layer](https://victorzhou.com/media/cnn-post/conv-gradient-example-2.svg)](https://victorzhou.com/media/cnn-post/conv-gradient-example-2.svg)

2. a max pooling layer that summarize image features [![max pooling](https://victorzhou.com/media/cnn-post/maxpool-forward.svg)](https://victorzhou.com/media/cnn-post/maxpool-forward.svg)

3. a softmax layer that turns arbitrary real values into probabilities [![softmax](https://i0.wp.com/dataaspirant.com/wp-content/uploads/2017/03/Softmax-Function-compressor.jpg)](https://i0.wp.com/dataaspirant.com/wp-content/uploads/2017/03/Softmax-Function-compressor.jpg?resize=500%2C500)


Every layer has a `forward` function to evaluate loss during training and a `backward` function to realize backpropagation. For more mathematical details, please refer to [Victor Zhou's work](https://victorzhou.com/blog/intro-to-cnns-part-1/).

The final test accuracy is of 64% with 64X64 grayscale images.


### Homework

This is the homework assignment of the 7th week for [Siraj Raval course](https://www.machinelearningcourse.io/courses/make-money).
