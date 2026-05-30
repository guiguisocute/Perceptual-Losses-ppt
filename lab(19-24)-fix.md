## 19

19需要重写一下：

 	1. 没有解释训练参数是什么， baseline篇幅过大，LR输入有点不明所以，重新读一下论文的这段：
     

```
In single-image super-resolution, the task is to generate a high-resolution output image from a low-resolution input. This is an inherently ill-posed problem, since for each low-resolution image there exist multiple high-resolution images that could have generated it. The ambiguity becomes more extreme as the super-resolution factor grows; for large factors (⇥4, ⇥8), fine details of the highresolution image may have little or no evidence in its low-resolution version.  To overcome this problem, we train super-resolution networks not with the per-pixel loss typically used [1] but instead with a feature reconstruction loss (see Section 3) to allow transfer of semantic knowledge from the pretrained loss network to the super-resolution network. We focus on ⇥4 and ⇥8 superresolution since larger factors require more semantic reasoning about the input.  The traditional metrics used to evaluate super-resolution are PSNR and SSIM [59], both of which have been found to correlate poorly with human assessment of visual quality [60–62]. PSNR and SSIM rely on low-level di↵erences between pixels, and PSNR operates under the assumption of additive Gaussian noise. In addition, PSNR is equivalent to the per-pixel loss `pixel, so as measured by PSNR a model trained to minimize per-pixel loss should always outperform a model trained to minimize feature reconstruction loss. We therefore emphasize that the goal of these experiments is not to achieve state-of-the-art PSNR or SSIM results, but instead to showcase the qualitative di↵erence between models trained with per-pixel and feature reconstruction losses.  Model Details. We train models to perform ⇥4 and ⇥8 super-resolution by minimizing feature reconstruction loss at layer relu2_2 from the VGG-16 loss network . We train with 288⇥288 patches from 10k images from the MS-COCO training set, and prepare low-resolution inputs by blurring with a Gaussian kernel of width = 1.0 and downsampling with bicubic interpolation. We train with a batch size of 4 for 200k iterations using Adam [56] with a learning rate of 1⇥10 3 without weight decay or dropout. As a post-processing step, we perform histogram matching between our network output and the low-resolution input.
```

## 20

首先把fig8放在左边自裁剪一下，并且要说明一下PSNR落后，我们22页再将

## 21

fig9.png放左边，但是不知要说有点，还要说明是伪影，棋盘格问题的原因等等，现在没说，但是论文有提到.

## 22

排版太烂，重新审美一下

## 23

参考feature-inversion-explainer%20(2).html和perceptual-loss-lineage%20(3).html，说明其实是三个大贡献的融合又快又好地解决了mage transformation的问题并在超分和风格迁移中的到了验证，

右侧的后续贡献可以再说详细一点
