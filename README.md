# DeRe-Net

by Wan Huan, Qinqin Wang, Jinshan Zeng, Xin Wei.


## 1. Introduction
Although the existing methods have made some progress in solving the problem of boundary ambiguity and small polyp neglect by generating boundaries or capturing detail information, they still have significant limitations due to their neglect of detail information. For example, Polyp-PVT extracts detail features only through the lowest-level features, resulting in the detail information existing in other low-layer neural networks being lost. Thus, polyp boundaries can't be well segmented or small polyps are overlooked, as shown in the regions separately framed by the yellow and red box in the second column of \Cref{Fig:Introduction}. In addition, although M2SNet and BDGNet can mitigate the blurry border or small polyps neglect problem to some extent, they still generate polyp segmentation with blurry edges (see the regions framed by yellow boxes in the third and fourth column of \Cref{Fig:Introduction}) and miss small polyps (see the regions framed by red boxes in the third and fourth column of \Cref{Fig:Introduction}). 

To well segment small polyps and polyps with obscure borders, a new polyp segmentation network called Details Restoration Networks (DeRe-Net) is proposed in this paper. The main idea of DeRe-Net is to exploit detail information as much as possible and effectively restore them to the highest-level features. To achieve this, a Details Saliency Enhancement Module (DSEM), Feature Seamless Integration Decoder (FSID) and Selective Feature Aggregation Module (SFAM) have been designed. DSEM is responsible for capturing detail information from the low-level features and enhancing them, and FSID takes responsibility for seamlessly combining the detail information and the high-level features. Additionally, SFAM selects the interrelated details and highest-level features, then aggregates them. We validate the superiority of our proposed network through rigorous experimental evaluations, demonstrating its effectiveness in polyp segmentation, especially for small polyps. 

## 2. Usage:
### 2.1 Recommended environment:
```
Python 3.8
Pytorch 1.7.1
torchvision 0.8.2
```
### 2.2 Data preparation:
Downloading training and testing datasets and move them into ./dataset/, which can be found in this [Google Drive](https://drive.google.com/file/d/1pFxb9NbM8mj_rlSawTlcXG1OdVGAbRQC/view?usp=sharing)/[Baidu Drive](https://pan.baidu.com/s/1OBVivLJAs9ZpnB5I2s3lNg) [code:dr1h].


### 2.3 Pretrained model:
You should download the pretrained model from [Google Drive](https://drive.google.com/drive/folders/1Eu8v9vMRvt-dyCH0XSV2i77lAd62nPXV?usp=sharing)/[Baidu Drive](https://pan.baidu.com/s/1Vez7iT2v_g7VYsDxRGE8HA) [code:w4vk], and then put it in the './pretrained_pth' folder for initialization. 

### 2.4 Training:
Clone the repository:
```
git clone https://github.com/DengPingFan/Polyp-PVT.git
cd Polyp-PVT 
bash train.sh
```

### 2.5 Testing:
```
cd DeRe-Net
bash test.sh
```

### 2.6 Evaluating your trained model:

Matlab: Please refer to the work of MICCAI2020 ([link](https://github.com/DengPingFan/PraNet)).

Python: Please refer to the work of ACMMM2021 ([link](https://github.com/plemeri/UACANet)).

Please note that we use the Matlab version to evaluate in our paper.


### 2.7 Well trained model:
You could download the trained model from [Google Drive](https://drive.google.com/drive/folders/1xC5Opwu5Afz4xiK5O9v4NnQOZY0A9-2j?usp=sharing)/[Baidu Drive](https://pan.baidu.com/s/1csPvdWqtbPBGrUWYO346Ug) [code:9rpy] and put the model in directory './model_pth'.

### 2.8 Pre-computed maps:
[Google Drive](https://drive.google.com/file/d/1L0pFFmd9fbqnJnBwrM9cEV5nlRS32mbQ/view?usp=sharing)/[Baidu Drive](https://pan.baidu.com/s/1UO1VaqXRRFNq23ku9yfMaw) [code:x3jc]



