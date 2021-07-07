# CIFAR-10
In this project I wrote two models to classify the [CIFAR-10 dataset](https://en.wikipedia.org/wiki/CIFAR-10). For the first model, I wrote a simple CNN network and trained it from scratch, to achieve an 80% accuracy on the test set (baseline is 10%). For the second model, I used a pretrained [VGG16 network](https://arxiv.org/pdf/1409.1556.pdf) with a few modifications, which yielded an 87% accuracy and converged much faster (3 epochs vs. 45).

![cifar10 image](https://user-images.githubusercontent.com/78589884/124727314-45030600-df17-11eb-9b80-80623f99d529.png)

The notebook [cifar10_keras.ipynb](https://github.com/masalha-alaa/cifar10-keras/blob/master/cifar10_keras.ipynb) includes the whole code for the two networks ***(refresh if it doesn't load)***. Although it contains a run and output only for my custom model, you can change the `MODEL_TYPE` parameter to run it with the VGG model. Moreover, I made another notebook for compraing the two models, in which you can see the outputs of the two models simultaneously. It can be found in this repository under the name [cifar10_keras_benchmark.ipynb](https://github.com/masalha-alaa/cifar10-keras/blob/master/cifar10_keras_benchmark.ipynb) ***(refresh if it doesn't load)***.

# Overview
## Custom CNN Model
![CNN Model](https://user-images.githubusercontent.com/78589884/124726896-da51ca80-df16-11eb-8794-b1af83c71592.png)

## Pretrained VGG16 Model
![VGG16 Model](https://user-images.githubusercontent.com/78589884/124727157-20a72980-df17-11eb-9391-a6ddf2ab8fc4.png)

Note how the model converges and starts overfitting just after 3 epochs. I could probably overcome the overfitting problem by adding Dropout and Batch Normalization layers, but the result (87%) prior to overfitting was satisfying enough. Besides, my goal was to compare a custom model with a true VGG model (which originally does not have those kind of layers).
