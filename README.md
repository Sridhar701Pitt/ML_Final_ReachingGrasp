Refer here if you want to use docker

https://github.com/ultralytics/yolov5/wiki/Docker-Quickstart

sudo docker pull ultralytics/yolov5:latest

sudo docker run --ipc=host --gpus all -it -v "$(pwd)"/datasets:/usr/src/datasets ultralytics/yolov5:latest

python train.py  # train a model
python val.py --weights yolov5s.pt  # validate a model for Precision, Recall and mAP
python detect.py --weights yolov5s.pt --source path/to/images  # run inference on images and videos
python export.py --weights yolov5s.pt --include onnx coreml tflite  # export models to other formats