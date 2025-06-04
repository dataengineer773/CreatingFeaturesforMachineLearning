We want to convert an image into an observation for machine learning, Use NumPy’s flatten to convert the multidimensional array containing an image’s data into a vector
containing the observation’s values Images are presented as a grid of pixels. If an image is in grayscale, each pixel is presented by one value
(i.e., pixel intensity: 1 if white, 0 if black). For example, imagine we have a 10 × 10–pixel image, In this case the dimensions of the images data will be 10 × 10,
And if we flatten the array, we get a vector of length 100 (10 multiplied by 10), data we will feed to our machine learning algorithms.
If the image is in color, instead of each pixel being represented by one value, it is represented by
multiple values (most often three) representing the channels (red, green, blue, etc.) that blend to make
the final color of that pixel. For this reason, if our 10 × 10 image is in color, we will have 300 feature
values for each observation, One of the major challenges of image processing and computer vision is that since every pixel location
in a collection of images is a feature, as the images get larger, the number of features explodes, As the output shows, even a small color image has almost 200,000 features, which can cause problems
when we are training our models because the number of features might far exceed the number of
observations.
This problem will motivate dimensionality strategies discussed in a later chapter, which attempt to
reduce the number of features while not losing an excessive amount of information contained in the
data.
