15：需要加入这个公式

![image-20260530124020965](C:\Users\zengs\AppData\Roaming\Typora\typora-user-images\image-20260530124020965.png)

并且要解释这个公式的内容，还要更详细话训练参数的表格描述：

1. 数据与训练配置

- 训练集：MS-COCO 数据集（约8万张图片，256×256分辨率）
- 优化器：Adam
- 学习率： 1 × 10⁻³
- Batch Size：4
- 迭代次数：40,000次（约2个epoch）
- 训练硬件：单张 GTX Titan X，每个风格训练约4小时
- 关键约束：每个风格单独训练一个网络，一次训练只能学会一种风格

1. 损失函数配置（核心细节）

- 内容损失（Feature Reconstruction Loss）：用VGG-16的 relu3_3 层特征，保证生成图和原图内容/结构一致

- 风格损失（Style Reconstruction Loss）：用VGG-16的 relu1_2、relu2_2、relu3_3、relu4_3 四层特征的Gram矩阵，捕捉多尺度风格纹理

- TV正则（Total Variation）：系数 10⁻⁶ ~ 10⁻⁴ ，平滑图像、减少噪点和锯齿

  


  16：

  ![16-fig7Example results for style transfer on 512 × 512 images by applying modelstrained on 256 × 256 images. The style images are the same as Figure 6](D:\GitHub Cave\Perceptual Losses\16-fig7Example results for style transfer on 512 × 512 images by applying modelstrained on 256 × 256 images. The style images are the same as Figure 6.png)

  ![16-fig6](D:\GitHub Cave\Perceptual Losses\16-fig6.png)

需要把这两张图嵌进去，尤其是16-fig6.png，左中右分别是content和gatys和ours，fig7则是展示训练后的分辨率无关性

17

左侧图片要换成：
![image-20260530124739298](C:\Users\zengs\AppData\Roaming\Typora\typora-user-images\image-20260530124739298.png)





18下方有点空：要把页面的布局调整一下，增大一下字体等等





