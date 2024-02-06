# Object-Detection-Framework
Custom Object Detection Framework 


## Using Yolov5

### Installing Yolov5 

    git clone https://github.com/ultralytics/yolov5
    cd yolov5
    pip install -r requirements.txt

python train.py --img 416 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt --cache
