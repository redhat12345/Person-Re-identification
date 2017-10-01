# Person Re-identification
Realization of Unlabeled Samples Generated by GAN Improve the Person Re-identification Baseline in vitro

https://arxiv.org/pdf/1701.07717.pdf

| Experiment    | Rank-1        | mAP           |
| ------------- | ------------- | ------------- |
| Baseline      | 72.71         | 49.14         |

Baseline: ResNet-50, cross-entropy loss, SGD, momentum = 0.9, learning rate for convolutional layers = 0.002, learning rate for fc layer  = 0.1, 30 epochs with 0.1 learning rate decay after 20th epoch

DCGAN

Some changes were made in the original code https://github.com/pytorch/examples/blob/master/dcgan/

I added additional layer to both generator and discriminator, so network input is 128x128 images

I used generator with 128 filters in last convolutional layer and discriminator with 32 filters in first convolutional layer
