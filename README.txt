README
Our project should be run in the following environment:
1. pytorch later than 1.0 (cuda available)
2. cuda 9.0

We have submit our training result and you can also train by yourself:
input in the command line:
python train.py --crop_size num(default is 88, representing the training image size)
                        --upscale_factor num(default is 4, representing how large you want to transform)
                        --num_epochs num(default is 10, representing the number of the training epochs)

For testing, you can transfrom your own LR  into HR:
input in the command line:
python test_image.py --upscale_factor num(default is 4)
                                  --test_mode char(default is GPU, representing whether you want to test by your GPU or CPU)
                                  --image_name char(your LR image name)
                                  --model_name char(netG_epoch_X_Y.pth, X represents the upscaling factor and 
                                     Y represents the training epoch, you can find the file in the 'epochs' file after training)
You can also see your loss and PSNR,SSIM in the 'statistic' file.
Thanks for use!