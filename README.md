## Prepare
Environment: PyTorch (0.4.0), torchvision (0.2.1), tensorboardX, python3, CUDA(8.0)   
•	git clone https://github.com/liuchunlei0430/CBCN_Pytorch.git
get the ImageNet dataset ready    
Install Convolutional Module and Binary Module    
•	cd install    
•	sh install.sh     
•	cd BinActivateFunc_PyTorch    
•	sh install.sh   

## Train and Evaluation
•	Train: python ImageNet.py [dataset_dir] --tensorboard   
•	Evaluation: python ImageNet.py [dataset_dir] --pretrained --tensorboard   
CBCN(without centerloss finetune) models can be obtained in https://drive.google.com/open?id=1wXL5LJAE6oduDBM7if4zeoSIJ0tjS4sS.   
CBCN(with centerloss finetune) is prepared to upload in Google Drive.   

| ResNet18 | Full-precision | CBCN(without centerloss finetune) | CBCN(with centerloss finetune) |
| ------ | ------ | ------ | ------ |
| Top-1 | 69.3 | 61.0 | 61.4 |

Thanks for the code of ORN! Inspired by ORN which already show their powerful ability in within-class rotation-invariance, we also employ similar way to enhance the representative ability which destoryed by the binarization process. We focus on storate reduction in our CBCNs. More detail can be seen in the install/orn/modules/ORConv.py.    

## Please cite    
@inproceedings{liu2019cbcn,   
  title={Circulant Binary Convolutional Networks: Enhancing the Performance of 1-bit
DCNNs with Circulant Back Propagation},   
  author={Liu, ChunLei and Ding, Wenrui and Xia, Xin and Zhang, Baochang and Gu, Jiaxin  and Liu, Jianzhuang and Ji, Rongrong and David, Doermann },    
  booktitle={IEEE Conference on Computer Vision and Pattern Recognition},   
  year={2019}   
}   
@ inproceedings{Zhou2017ORN,    
    author = {Zhou, Yanzhao and Ye, Qixiang and Qiu, Qiang and Jiao, Jianbin},    
    title = {Oriented Response Networks},   
    booktitle = {CVPR},   
    year = {2017}   
}

