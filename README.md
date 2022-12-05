# OvaryTreatment_AnginPKM2VEGF

## Setup

#### Requirerements
- ubuntu 18.04
- RAM >= 16 GB
- GPU Memory >= 10 GB
- GPU driver version >= 418.56
- CUDA version >= 10.1
- cuDNN version >= 7.6.4

#### Download
Execution file, configuration file, and models are download from the [zip](https://drive.google.com/file/d/1Rj0OZClt0esA86NJqubM1nXABWdXmyZd/view?usp=sharing) file.  (For reviewers, please use the manuscript ID CTM.............28 as the password to decompress the file.)

#### File structure
```
OvaryTreatment_AnginPKM2VEGF/
│
├── Data/ - training and testing data location
│   ├── invalid-PKM2_0/
│   │   ├── 10_2.bmp
│   │   ├── 10_3.bmp
│   │   ├── 10_4.bmp
│   │   │       ⋮
│   │   └── 20_11.bmp
│   │
│   ├── invalid-PKM2_2/
│   │   ├── 39_2.bmp
│   │   ├── 39_3.bmp
│   │   ├── 39_4.bmp
│   │   │       ⋮
│   │   └── 48_11.bmp
│   │
│   ├── effective-PKM2_9/
│   │   ├── 91_2.bmp
│   │   ├── 91_3.bmp
│   │   ├── 91_4.bmp
│   │   │       ⋮
│   │   └── 101_12.bmp
│   │
│   └── effective-PKM2_21/
│       ├── 91_13.bmp
│       ├── 91_14.bmp
│       ├── 91_15.bmp
│       │       ⋮
│       └── 100_22.bmp
│
├── Detection_ROI/ - detect the tissue core 
│   ├── input_img/ - put the SVS file
│   │   └── effective-PKM2.svs/
│   │       ├── setting.json - configuration file
│   │       └── effective-PKM2.svs
│   ├── model/ - model of the detector
│   │   └── _iter_100.caffemodel
│   ├── ClassId.txt
│   ├── caffe_root.txt - set the caffe root
│   ├── deploy_roi.prototxt
│   ├── detected2.json - configuration file
│   └── Main_Detection_ROI - execution file
│
├── BB_Segmentation - extract the tumor tissue
│   ├── AfterSeg_BB_tileout/ - storage location of tumor patches
│   ├── BB_tileout/ - storage location of normal patches
│   ├── model/ - model of the segmentation
│   │   └── TMAIHC_All_i30w.caffemodel
│   ├── deploy.prototxt
│   ├── caffe_root.txt - set the caffe root
│   └── Main_Segmentation - execution file
│
├── List_Preprocessing/
│   └── Main_List_Preprocessing - execution file
│
├── List/ - demo list
│   ├── TestingList_all.txt
│   ├── TestingList_attentionScoring.txt
│   ├── TrainingList_all.txt
│   └── TrainingList_filter.txt
│
├── Trainining/
│   ├── Model - storage location of training models
│   ├── slover.py - execution file
│   ├── solver.prototxt - configuration file
│   ├── train.prototxt
│   ├── voc_layers.py
│   └── voc_layers.pyc
│
└── Testing/ 
    ├── model - demo model
    │   └── PKM2_proposed.caffemodel
    ├── deploy.prototxt
    └── inference_TMA.py - execution file



```
