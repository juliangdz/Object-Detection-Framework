# Object-Detection-Framework
Custom Object Detection Framework 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Using Yolov5

### Installing Yolov5 

    git submodule update --init --recursive
    cd yolov5
    pip install -r requirements.txt

### Training Yolov5

    cd yolov5
    python train.py --img 416 --batch 16 --epochs 50 --data ../dataset.yaml --weights yolov5s.pt --cache

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Using MMDet

### Setup MMDetection

    conda create -n mmdetection python=3.8.16
    conda activate mmdetection
    git clone https://github.com/open-mmlab/mmdetection.git
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