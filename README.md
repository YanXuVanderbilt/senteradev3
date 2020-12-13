# senteradev3

This is about estimating the calibration matrix for sentera via a neural network. 

Sentera produces two images for each scene, RGB and NIR, 6 channels in total. So input for the NN has dim 6. The output of first linear layer should be the 2 values we use to calculate NDVI, i.e. (NIR - RGB) / (NIR + RGB). So first layer is a (6, 2).

After fc1, the NN has a custom layer inheritted from nn.Module (we are using PyTorch) which is based on NDVI. 

The activation function is also custom, where we say 0.3 - 0.8 is NDVI value for healthy. 

## To run the code

Start with Model1.py


