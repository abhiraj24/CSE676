<p align="center">
  <img src="SRWGAN GP SSIM-logos_transparent.png" height=500>
</p>

# CSE676: Super Resolution WGAN with Gradient Penalty and Structural Similarity for Image Restoration
Super-Resolution Generative Adversarial Networks (SRGAN) are powerful generative models for recovering the detail finer texture in the images. However, sometimes we encounter problems such as training instability, generator loss and discriminator loss cannot converge, the final output of the generator is unsatisfactory. In this paper, we implement Wasserstein GAN-Gradient Penalty (WGAN-GP) into SRGAN to improve the unstable training process, basically solve the problem of collapse mode, ensure the diversity of generated samples, reduce the possibility of vanishing or exploding gradients. Additionally, we used total variation loss (TV loss) and structural similarity index measure (SSIM) into the generator objective function to improve the results of generator, which in turn improve the whole model. Our results demonstrate that our model offers great performance of Image Restoration. 

Colab Link to Project: [Colab Demo](https://colab.research.google.com/drive/1R-7UojfD2oHKiqUWDRFYZ7CjjOCNMiuu?usp=sharing)


### Steps to Run 

- ✅ Open the Colab link to the code for accessing the Google colab version.
- ✅ Upload the test images which will be used for testing the model performance to the colab file section.
- ✅ Download the Test dataset from [Kaggle](https://www.kaggle.com/datasets/landzz/llsrdatasets)
- ✅ Upload the Zip folder to the colab file section and name it as Test Dataset.zip
- ✅ The training and validation set will be downloaded into the colab by itself.
  



### Results
| Model | SR-WGAN GP +SSIM  | SR-WGAN GP  |
| :---:   | :-: | :-: |
| PSNR | 25.37 | 21.33 |

We ran two different types of models where we incorporated the SSIM loss in one model and kept it out in another. It can be seen from Table 1 that SRWGAN with SSIM was better. 

<p align="centre">
  <img src="butterflyx4.png" height=300>
</p>

We could see the perceptual variation between the two models when we compared the Set5 images. The SRWGAN without SSIM have loss in tint and contrast whereas SRWGAN+SSIM have kept the contrast values
