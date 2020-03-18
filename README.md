# Neural Style Transfer

This project is an implementation of NST algorithm that generates artistic images.

 ## 1 - Problem Statement

Neural Style Transfer (NST) is one of the most fun techniques in deep learning. As seen below, it merges two images, namely, a "content" image (C) and a "style" image (S), to create a "generated" image (G). The generated image G combines the "content" of the image C with the "style" of image S. 

![Monet](https://github.com/parasgulati8/Convolution-Neural-Network/blob/master/Neural%20Style%20Transfer/images/perspolis_vangogh.png)

## 2 - Transfer Learning

Neural Style Transfer (NST) uses a previously trained convolutional network, and builds on top of that.

Following the original NST paper (https://arxiv.org/abs/1508.06576), we used the VGG-199 network. This model has already been trained on the very large ImageNet database, and thus has learned to recognize a variety of low level features (at the earlier layers) and high level features (at the deeper layers).

## 3 - Neural Style Transfer 

We will build the NST algorithm in three steps:

- Build the content cost function ![](https://render.githubusercontent.com/render/math?math=J_%7Bcontent%7D%28C%2CG%29&mode=inline)
- Build the style cost function ![](https://render.githubusercontent.com/render/math?math=J_%7Bstyle%7D%28S%2CG%29&mode=inline)
- Put it together to get ![](https://render.githubusercontent.com/render/math?math=J%28G%29%20%3D%20%5Calpha%20J_%7Bcontent%7D%28C%2CG%29%20%2B%20%5Cbeta%20J_%7Bstyle%7D%28S%2CG%29&mode=inline)

## 4 - Solving the optimization problem
Finally, let's put everything together to implement Neural Style Transfer!

Here's what the program will have to do:

1. Create an Interactive Session
2. Load the content image 
3. Load the style image
4. Randomly initialize the image to be generated 
5. Load the VGG19 model
7. Build the TensorFlow graph:
    - Run the content image through the VGG19 model and compute the content cost
    - Run the style image through the VGG19 model and compute the style cost
    - Compute the total cost
    - Define the optimizer and the learning rate
8. Initialize the TensorFlow graph and run it for a large number of iterations, updating the generated image at every step.

## Results

Here are few other examples:

- The beautiful ruins of the ancient city of Persepolis (Iran) with the style of Van Gogh (The Starry Night)
![](https://github.com/parasgulati8/Convolution-Neural-Network/blob/master/Neural%20Style%20Transfer/images/louvre_generated.png)

- The tomb of Cyrus the great in Pasargadae with the style of a Ceramic Kashi from Ispahan.
![](https://github.com/parasgulati8/Convolution-Neural-Network/blob/master/Neural%20Style%20Transfer/images/pasargad_kashi.png)

- A scientific study of a turbulent fluid with the style of a abstract blue fluid painting.
![](https://github.com/parasgulati8/Convolution-Neural-Network/blob/master/Neural%20Style%20Transfer/images/circle_abstract.png)
