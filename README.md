
This is the test code for IJCAI 2019 submission

Testing:
Step 1: download the compressed model from [Baidu Yun model]() or [Google Driver model]()
and put it in the root folder and unzip it.

Step 2: Run test_vocspsm_vgg.py for SGIR-vgg16 evaluation, the predictions will be saved in SAVE_DIR = './result/'. Mean IoU of 58.8 can be achieved.

Step 3: Run test_vocspsm_resnet for SGIR-resnet101 evaluation, the predictions will be saved in SAVE_DIR = './result/'. Mean IoU of 64.0 can be achieved.

Step 4:  Please refer to Deeplabv2 for runing CRF as post-processing. The mean IoU of 61.4 and 64.8 can be achieved for SGIR-vgg16 and SGIR-resnet101, respectively. 
The released results on PASCAL VOC 2012 val and test datasets are contained in [Baidu Yun dataset]() or [Google Driver dataset]()

Step 5: we have provided the matlab code for evaluation. You can evaluate the resutls and obtain Iou youself. Please refer to https://github.com/zmbhou/IoUeval.
