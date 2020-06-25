# mnist_digit_gan

##Summary

### Training Discriminator

Get half samples from dataset, half samples from generated samples using Generator. y = 1 for all dataset samples, 0 for all generated samples.

### Training Generator

We cannot train generator alone since we rely on discriminator. Therefore we freeze discriminator weights and create a new combined model (Generator followed by Discriminator) so the image we input is mutated via generator and passed to Discriminator for classification result. y = 1 for all samples since that is the goal of the generator.
