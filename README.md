
This is the test code for IJCAI 2019 submission "Saliency Guided Iterative Training for Weakly Supervised Semantic Segmentation"

Testing:
====
Step 1: download the compressed model from [Baidu Yun model](https://pan.baidu.com/s/1DEyToD1iLLfCDa-cIQS4gQ) with password:bg15 or [Google Driver model](https://drive.google.com/file/d/1zAzeztLJIPLvVKt2sKgfoued6tXgFCwC/view?usp=sharing)
and put it in the root folder and unzip it. We have release all the models corresponding to steps P1 to P4 presented in Table.6 in the sumbitted manuscript [Baidu Yun model](https://pan.baidu.com/s/1KFZd-AWMf0-FsW6SLaDP4g) with password:y970.

Step 2: Change the root for retored model and Run test_vocSGIR_vgg.py for SGIR-vgg16 evaluation, the predictions with multiscale fusion will be saved in SAVE_DIR = './result/'. Mean IoU of 59.3 can be achieved on PASCAL VOC 2012 validation dataset.

Step 3: Change the root for retored model and Run test_vocSGIR_resnet for SGIR-resnet101 evaluation, the predictions with multiscale fusion will be saved in SAVE_DIR = './resultresnet/'. Mean IoU of 64.0 can be achieved on PASCAL VOC 2012 validation dataset.

Step 4:  Please refer to https://github.com/xtudbxk/semantic-segmentation-metrics for runing CRF as post-processing. 

Step 5: we have provided the matlab code for evaluation. You can evaluate the resutls and obtain Iou youself. Please refer to https://github.com/zmbhou/IoUeval.

Results: 
====
The mean IoU of 61.4 and 64.8 can be achieved for SGIR-vgg16 and SGIR-resnet101, respectively on the PASCAL voc 2012 validation dataset. The mean IoU of 62.3 and 65.4 can be achieved for SGIR-vgg16 and SGIR-resnet101, respectively on the PASCAL voc 2012 test dataset. 

Figure 1: Illustration of Four States in the Process of Training Samples Updating:
====
![image](https://github.com/zmbhou/SGIR/blob/master/picture/iterativeGTs.png)

Q1 stands for the quality of the initial proxy GTs used for iteration 0;
Q2 stands for the quality of the refined proxy GTs genrated by the updated segmentation model in the iterative retraining process.
Q3 stands for the quality of the proxy GTs refined by saliency.

In state 1, Q1<Q2<Q3

In state 2,  Q1<Q2, Q2>Q3

In state 3, Q1>Q2, Q3>Q2

In state 4, Q1>Q2>Q3.

Figure 2: Visual Comparison between Different Methods<br />
====
![image](https://github.com/zmbhou/SGIR/blob/master/picture/visialcomparison2.png)
The results of DSRG and SEENET are generated by our reproductions. The red rectangle highlights the refined or discovered regions.

DSRG is the method proposed in CVPR 2018 paper "Weakly-Supervised Semantic Segmentation Network with Deep Seeded Region Growing"

SEENET is the method proposed in NIPS 2018 paper "Self-Erasing Network for Integral Object Attention"


