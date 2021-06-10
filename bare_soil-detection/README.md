Training data from LUCAS dataset is used to train one autoencoder that reconstructs bare soil. All landcovers that are not well reconstructed should be not bare soil. All pixels well reconstructed should be bare soil. 

Link to LUCAS:
https://esdac.jrc.ec.europa.eu/projects/lucas
### Worflow

1- Train autoencoder with LUCAS database
  1.1.) Download LUCAS data from [here](https://esdac.jrc.ec.europa.eu/content/lucas2015-topsoil-data#tabs-0-description=0)

2- Predict and get the error

3- Discriminate between bare soil and other land covers

  a) kmeans over error bands array
  
  b) sum all bands error and make segmentation
  
    b.1) Ideas segmentación de imágenes
    b.2) Grey scale: imagen de una banda con valores continuos
    b.3) https://nl.mathworks.com/help/images/marker-controlled-watershed-segmentation.html
    
 
### Applications
- Bare soil detection
- Deforestation (paper?)
    
