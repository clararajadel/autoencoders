
This folder contains the code, autoencoder models and figures resulting from the application of autoencoders in the area of Branau.

DATE: 22-03-2021 (last modification)

DETAILS:
- Area of study: Branau
- Name (or objective): basic
- Without hazzy images: False
- Number of clusters: 8
- Number of training pixels per cluster: 100
- Random testing: True
- Number of hidden layers: 1
- Number of neurons in hidden layers: 10
- Optimizer: Adam
- Learning rate: 0.01
- Activation function: linear

DESCRIPTION

See why clouds are well reconstructed but show error. Our hypotesis is that bands bad reconstructed are no visible ones.
In Branau the training data we have is few and bad quality. That's why I select 100 pixels per cluster for training and 100 for testing.
I do another clustering over the testing image to detect pixel positions where are clouds.

