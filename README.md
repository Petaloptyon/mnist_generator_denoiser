In this repository you can see my trials to do gan by using many denoisers. 
How it works: 
 - create dataset from datasets, by adding little noise to all images from preveous dataset, starting from initial train dataaset;
 - create denoisers (using autoencoder)
 - train denoisers to remove noise by a little
 - create connection layers (to connect denoisers)
 - constract GAN from connection layers and denoisers
 - train gan

During training gan with different architectures of connection models, i notice, that connection model must pick out main points from pictures. When i use same or more complex conntion layers as denoisers, result instantly became evarage (gan start to predicting the averaged results over the entire dataset). Also when i trained denoisers, train connection layers, create gan, start train all model (all weights was trainable) result start becoming evarage. 

To sum it all up, how do I train my gun? I experimented a bit and came to the conclusion that the best way to train it is: (1) train denoisers -> (2) train connecting layers only on neighboring denoiser models -> (3) build a gun from all pre-trained models -> (4) train gun with non-trainable denoiser weights -> (5) train gan with all trainable weights. BUT, when I started building, I made a small mistake: I added every second denoiser and its connecting layer to the model (you can see more in the code), and this mistake improved my model, it became better to draw.

Here is the reuslt of third train (when i train full gan):

![gan_denoiser_3](https://github.com/Petaloptyon/mnist_generator_denoisers/assets/131547274/c40f6a06-470c-4531-a6ff-43e895846ade)

Perhaps if I had more resources on google colab I would train it better, but already now you can consider some numbers (9, 7, 0, 3, 8, 4)

If you want to run my Gan you should do it on google colab. Sorry for not attaching weights, but I can't upload files to github that weigh more than 25 MB

############################### now i am iproving model ###############################
