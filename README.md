# Cat vs non-cat image classifier

Image classification is an important computer vision problem. Here, we have a two-class problem where we want to classify a given image as containing a cat or not. We build two neural networks for this classification task and compare their classification performance.

## Datasets
We have 209 training examples and 50 test examples, where each example is of shape (64, 64, 3) with each of RGB channel image is of size 64x64. The examples are labeled 1 for a cat and 0 for anything other than a cat. To input these examples into a neural network, we reshape each color image into a vector by flattening, as shown below.

![Image to vector conversion of input](images/imvectorkiank.png)

## Two-layer neural network
This model has only two layers: INPUT -> LINEAR -> RELU -> LINEAR -> SIGMOID -> OUTPUT.

![Two-layer model architecture](images/2layerNN_kiank.png)

After 2500 iterations this model shows the training accuracy is 1.0 and the test accuracy of 0.72.

## L-layer deep neural network
This model has L layers: INPUT -> L[INEAR -> RELU] x (L-1) -> LINEAR -> SIGMOID -> OUTPUT.

![L-layer model architecture](images/LlayerNN_kiank.png)

After 2500 iterations this model (with 4 layers) shows the training accuracy of 0.99 and the test accuracy of 0.8, which is better than that of the two-layer model.
