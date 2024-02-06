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