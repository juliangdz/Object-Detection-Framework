# Object-Detection-Framework

- **Student ID**: 437451
- **Student Name**: Julian Gerald Dcruz
- **Course Code**: N-AAI-DAV-23-A23
- **Deep Learning Assignment**

## Dataset

    RAW Dataset: 
        images-directory: data/image
        labels-directory: data/label
    
    UAV_DATASET: (Resized Images to 416x416 / Rescaled and Normalized Bounding Box Coordinates)
        test/train/val : in YOLO Format 
    
    UAV_DATASET: 
            KITTI_FORMAT: in MMDetection Format

Use 'data_loading.ipynb' for visualization of dataset and conversion

## Using Yolov5

### Installing Yolov5 

    git submodule update --init --recursive
    cd yolov5
    pip install -r requirements.txt

### Training Yolov5

    Modify the dataset.yaml to include absolute paths to the dataset for train and val 
    cd yolov5
    python train.py --img 416 --batch 16 --epochs 50 --data ../dataset.yaml --weights yolov5s.pt --cache


## Using MMDet

MmDetection Version: 2.28.2

### Setup MMDetection

    conda create -n mmdetection python=3.8.16
    conda activate mmdetection
    git submodule update --init --recursive
    pip install  torch==1.9.0+cu111 torchvision==0.10.0+cu111 -f https://download.pytorch.org/whl/torch_stable.html
    pip install mmcv-full -f https://download.openmmlab.com/mmcv/dist/cu111/torch1.9.0/index.html
    cd mmdetection
    git checkout 2.x
    pip install -v -e .
    pip install -U wandb
    pip install notebook
    pip install ipykernel
    python -m ipykernel install --user --name mmdetection --display-name mmdetection

### Train and Log 

    Run Notebook: Train_Object_Detector_with_MMDetection_and_W&B.ipynb

## Wandb Report

- UAV Detection with Faster R-CNN Report: [here](https://api.wandb.ai/links/juliangeralddcruz/ybqf8nl9)
- UAV Detection with YOLOv5 Report: [here](https://api.wandb.ai/links/juliangeralddcruz/ekebtjj5)