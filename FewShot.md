包括Unsupervised, Weakly supervised, Few shot, Zero shot等topic <Br>
主要关注图像增强, 修复, 生成等任务

可能与其它方向的论文记录有重叠.

# Table of Contents
- [Unsupervised and Weakly Supervised](#unsupervised-and-weakly-supervised)



# Unsupervised and Weakly Supervised
#### LIR-for-Unsupervised-IR ★☆
**[Paper]** (CVPR 2020) Learning Invariant Representation for Unsupervised Image Restoration <Br>
**[Author]** Wenchao Du, Hu Chen, Hongyu Yang  <Br>
**[[Pytorch-Code](https://github.com/Wenchao-Du/LIR-for-Unsupervised-IR)]** <Br>**(无监督, domain transfer)**  无监督图像恢复, 使用了GAN, 设计了各种loss

#### *Bringing Old Photos Back to Life* ★★☆
**[Paper]** (CVPR 2020 Oral) Bringing Old Photos Back to Life <Br>
**[Author]** [Ziyu Wan](http://raywzy.com/), [Bo Zhang](https://www.microsoft.com/en-us/research/people/zhanbo/), [Dongdong Chen](http://www.dongdongchen.bid/), [Pan Zhang](https://panzhang0212.github.io/), [Dong Chen](https://www.microsoft.com/en-us/research/people/doch/), [Jing Liao](https://liaojing.github.io/html/), [Fang Wen](https://www.microsoft.com/en-us/research/people/fangwen/)  <Br>
**[[Project](http://raywzy.com/Old_Photo/)]** <Br>**(无监督, domain transfer)**  无监督老照片恢复, 用生成的老照片训练, 在真实老照片上取得好效果. 使用一个VAE将真实和生成的照片映射到相近的空间, 第二个VAE负责恢复无损照片, 中间还有一些映射等操作. 

#### Syn2Real ★★
**[Paper]**  (CVPR 2020) Syn2Real Transfer Learning for Image Deraining using Gaussian Processes<Br>
**[Author]** [Rajeev Yasarla](https://sites.google.com/view/rajeevyasarla/home), [Vishwanath A. Sindagi](https://www.vishwanathsindagi.com/), [Vishal M. Patel](https://engineering.jhu.edu/ece/faculty/vishal-m-patel/) <Br>
**[[Pytorch-Code](https://github.com/rajeevyasarla/Syn2Real)]**<Br>**(transfer learning, 高斯过程)**  使用高斯过程计算无标签真实数据的unsupervised loss. 从paper的实验效果来看有不错的效果, 值得一试

#### GLeNet ★★
**[Paper]** (ECCV 2020) Global and Local Enhancement Networks for Paired and Unpaired Image Enhancement <Br>
**[Author]** Han-Ul Kim, Young Jun Koh, Chang-Su Kim <Br>
**[[Project](http://mcl.korea.ac.kr/research/hukim-eccv2020-glenet/)]**   **[[Pytorch-Code](https://github.com/dongkwonjin/GleNet)]** <Br>**(无监督, 曲线预测)**  全局预测曲线(3*256) + 局部增强. 无监督训练部分采用类似cycle gan的策略. 更具有实用性的曲线预测策略已经开始获得关注, 相关论文越来越多了.

#### DGP ★★
**[Paper]** (ECCV 2020 Oral) Exploiting Deep Generative Prior for Versatile Image Restoration and Manipulation <Br>
**[Author]** [Xingang Pan](https://xingangpan.github.io/), [Xiaohang Zhan](https://xiaohangzhan.github.io/), [Bo Dai](http://daibo.info/), [Dahua Lin](http://dahua.site/), [Chen Change Loy](http://personal.ie.cuhk.edu.hk/~ccloy/), [Ping Luo](http://luoping.me/) <Br>
**[[Pytorch-Code](https://github.com/XingangPan/deep-generative-prior)]** <Br>
**(online finetune, 无需训练样本对)**  提出用预训练的GAN作为先验, 无需在特定任务上finetune, 即可实现超分, 上色等图像恢复任务和图像变形，类别转换等图像编辑功能. 论文主要是在一般GAN inversion的基础上, 提出同时优化隐向量z和生成网络参数, 达到了更好更自然的效果.

#### KernelGAN ★★
**[Paper]**  (NIPS 2019 Oral) Blind Super-Resolution Kernel Estimation using an Internal-GAN <Br>
**[Author]** Sefi Bell-Kligler, [Assaf Shocher](http://www.wisdom.weizmann.ac.il/~/assafsho/), [Michal Irani](https://www.weizmann.ac.il/math/irani/) <Br>
**[[Project](http://www.wisdom.weizmann.ac.il/~vision/kernelgan/)]** **[[Pytorch-Code](https://github.com/sefibk/KernelGAN)]**  <Br>**(zero-shot, 降质核估计)**  无监督预测降质核并进行超分的方法. 使用若干个现象卷积层的GAN预测降质kernel, 训练的的GAN可以合成一个kernel, 作为该图形的降质核, 网络训练采用LSGAN和若干正则项构成. 预测的模糊核作为ZSSR的降质核, 再无监督地预测炒粉结果

#### WESPE ★
**[Paper]** (CVPRW 2018) WESPE: Weakly Supervised Photo Enhancer for Digital Cameras <Br>
**[Author]** Andrey Ignatov, Nikolay Kobyshev, Radu Timofte , Kenneth Vanhoey, Luc Van Gool  <Br>
**[[Project](http://people.ee.ethz.ch/~ihnatova/index.html)]**   <Br>
**(无需训练样本对)**

#### Deep Photo Enhancer ★☆
**[Paper]** (CVPR 2018 Spotlight) Deep Photo Enhancer: Unpaired Learning for Image Enhancement from Photographs with GANs <Br>
**[Author]** [Yu-Sheng Chen](https://www.cmlab.csie.ntu.edu.tw/~nothinglo/), [Yu-Ching Wang](https://www.cmlab.csie.ntu.edu.tw/~urchinwang/), [Man-Hsin Kao](https://www.cmlab.csie.ntu.edu.tw/~cindy0711/), [Yung-Yu Chuang](https://www.csie.ntu.edu.tw/~cyy/) <Br>
**[[TF-Code](https://github.com/nothinglo/Deep-Photo-Enhancer)]** **[[TF-Code2](https://github.com/pnbao/deep-photo-enhance)]**<Br>**(无需训练样本对)**  UNet + cycGAN, 无需paired样本的图像增强方法, 可以参考, 只是代码有一点点乱

#### Deep Image Prior ★★
**[Paper]** (CVPR 2018) Deep Image Prior <Br>
**[Author]** [Dmitry Ulyanov](https://dmitryulyanov.github.io/about), [Andrea Vedald](https://www.robots.ox.ac.uk/~vedaldi/), [Victor Lempitsky](http://sites.skoltech.ru/compvision/members/vilem/)<Br>
**[[Project](https://dmitryulyanov.github.io/deep_image_prior)]**  <Br>
**(zero-shot)**
1) 一篇有趣的论文, 提出深度卷积网络在图像生成和恢复任务中表现好的原因, 可能并不是因为其从大量图像中学习到了某种先验, 其实随机初始化的网络足以从输入中抓取大量的low-level图像先验信息. 在通过迭代的方式从图像中学习先验的过程中, 那些自然的, 有规律的内容较容易提取,会先被学习出来, 因此就达到了去噪或其它restoration的目的. <Br>
2) 粗读, 实用性有待验证, 有时间可以好好研究一下. <Br>
