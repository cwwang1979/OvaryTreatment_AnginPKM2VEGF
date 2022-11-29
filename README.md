#OvaryTreatment_AnginPKM2VEGF

## Setup

#### Requirerements
- ubuntu 18.04
- RAM >= 16 GB
- GPU Memory >= 10 GB
- GPU driver version >= 418.56
- CUDA version >= 10.1
- cuDNN version >= 7.6.4

#### Download
Execution file, configuration file, and models are download from the [zip](address) file.  (For reviewers, please use the manuscript ID CTM.............28 as the password to decompress the file.)

#### File structure
```
OvaryTreatment_AnginPKM2VEGF/
│
├── BB_Segmentation
│   ├── AfterSeg_BB_tileout/
│   ├── BB_tileout/
│   ├── model/
│   │   └── TMAIHC_All_i30w.caffemodel
│   ├── deploy.prototxt
│   └── getDectorbbox.py
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
├── Detection_ROI/
│   ├── input_img/
│   │   ├── Ann.json
│   │   └── effective-PKM2_200x.svs
│   ├── model/
│   │   └── _iter_100.caffemodel
│   ├── ClassId.txt
│   ├── deploy_roi.prototxt
│   ├── detected2
│   └── Picture_test_all_TMA
│
├── List/
│   ├── TestingList.txt
│   ├── TestingList_highest.txt
│   └── TrainingList.txt
│
├── List_Preprocessing/
│   ├── attentionScoring.py
│   └── filter.py
│
├── Testing/
│   ├── model
│   │   ├── Angin_proposed.caffemodel
│   │   ├── PKM2_proposed.caffemodel
│   │   └── VEGF_proposed.caffemodel
│   ├── deploy.prototxt
│   └── inference_TMA.py
│
└── Trainining/
    ├── Model
    ├── slover.py
    ├── solver.prototxt
    ├── train.prototxt
    ├── voc_layers.py
    └── voc_layers.pyc

```
