# mnist_digit_gan

##Summary

### Training Discriminator

Get half samples from dataset, half samples from generated samples using Generator. y = 1 for all dataset samples, 0 for all generated samples.

### Training Generator

We cannot train generator alone since we rely on discriminator. Therefore we freeze discriminator weights and create a new combined model (Generator followed by Discriminator) so the image we input is mutated via generator and passed to Discriminator for classification result. y = 1 for all samples since that is the goal of the generator.

### Training format
for each epoch => we iterate over all images over EPOCH times. 
for each batch_per_epoch => we subdivide all images in dataset into batches, and we then iterate over each of these batches
for each iter => we train on each of these epochs over some number of iterations. this is also where we calculate our loss function per each iteration.
