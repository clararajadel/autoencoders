# Autoencoders
In this repository autoencoders are trained for landcover change detection through remote sensing. Autoencoders are neural networks based in a basic encode and decode processing. Difference detection is based in the disability of autoencoders to decode data never seen before.

Basic concepts about neural networks and autoencoders in PowerPoint: https://drive.google.com/file/d/1YdSS2BEUU4jjvz_a80ezKLsgaTq2f0vY/view?usp=sharing
## Training data
- Sentinel 2 images from DataCube (EODC) bands B1, B2, B3, B4, B5, B6, B7, B8, B8A, B9, B11, B12, DOY.
- The AOI (area of interest) are regions in Austria such as: Strober, Carinthia or Branau.

## Workflow
Different autoencoders are trained to decode different landcovers. Because the process is unsupervised clustering is done to assign different landcovers.

![Optional Text](../master/myFolder/image.png)

## Results
- Ideally one autoencoder per pixel would result in the best reconstruction. However, that would require an untenable training. In an AOI of 200 * 350 px, 25 autoencoders (one per pixel) performed much better than 8 autoencoders, but increasing to 100 autoencoders did not show as much improvement.
- Feature extraction using PCA does not make big improvements in reconstruction. It accelerates the process but it also increased noise in the reconstruction error in Strobbler area. Link: https://drive.google.com/file/d/1nMPb_T5T_y2P8YekFFHyM69SYuIIb-_w/view?usp=sharing
- Hazy training images worsen reconstructions and favour the usefulness of fewer autoencoders. Using clean training images is crucial.
- Data should be scaled (e.g. sklearn.preprocessing.MinMaxScaler).

## Next steps
- Cloudy pixels (which are not trained) give high error but in the TCC are well reconstructed. See what happens in other spectral bands.
- Unstable landcovers over time (e.g. seasonal crops) are not well reconstructed. Re-cluster over unstable areas to increase the number of autoencoders. Clusters to be reclustered in more groups can be selected based in their data distribution (max, min, mean...)
- Is clustering really helping? a) try random testing without clusters, b) telect training pixels manually.
