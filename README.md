In this repository you can see my trials to do gan by using many denoisers. 

How it works: 
 - create dataset from datasets, by adding little noise to all images from preveous dataset, starting from initial train dataaset;
 - create denoisers (using autoencoder)
 - train denoisers to remove noise by a little
 - create connection layers (to connect denoisers)
 - constract GAN from connection layers and denoisers
 - train gan
