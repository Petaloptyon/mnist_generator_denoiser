In this repository you can see my trials to do gan by using many denoisers. 
How it works: 
 - create dataset from datasets, by adding little noise to all images from preveous dataset, starting from initial train dataaset;
 - create denoisers (using autoencoder)
 - train denoisers to remove noise by a little
 - create connection layers (to connect denoisers)
 - constract GAN from connection layers and denoisers
 - train gan

During training gan with different architectures of connection models, i notice, that connection model must pick out main points from pictures. When i use same or more complex conntion layers as denoisers, result instantly became evarage (gan start to predicting the averaged results over the entire dataset). Also when i trained denoisers, train connection layers, create gan, start train all model (all weights was trainable) result start becoming evarage.
 
############################### now i am iproving model ###########################
