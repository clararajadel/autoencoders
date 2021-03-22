
This folder contains the code, autoencoder models and figures resulting from the application of autoencoders in the area of Strobler.

DATE: 22-03-2021 (last modification)

DETAILS:
- Area of study: Strobler
- Name (or objective): basic
- Without hazzy images: True
- Number of clusters: 8
- Number of training pixels per cluster: 1
- Random testing: True
- Number of hidden layers: 1
- Number of neurons in hidden layers: 10
- Optimizer: Adam
- Learning rate: 0.01
- Activation function: linear

DESCRIPTION

As increasing the number of clusters the error in the prediction decreases. The objective is to increase the number of AEs in those areas where the variability is higher (usually crops). For that the mean, max, min values for each cluster will be calculated and the most variable clusters will be reclustered.
Note that in the case of Strobler the most variable clusters are forest.

