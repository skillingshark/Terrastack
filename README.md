# Terrastack
Terrastack Satellite Agri-Modeling


First, we have preprocessed the data to find that the average size of 4 cross 36 cross 36

We convert image data to tensor

Then we used Variational autoencoder using CNN:

This model encodes tensor image to a lower dimension and then decodes it back to the original dimension.

This model is widely used to remove noise and to get a latent vector which is the bottleneck that has a lower dimension.

So basically we used this latent vector to clustering

We used the Gaussian mixture model for cluster

A Gaussian mixture model is a probabilistic model that assumes all the data points are generated from a mixture of a finite number of Gaussian distributions with unknown parameters.

this model uses latent vectors obtained from VAE and clusters them into 3 classes
