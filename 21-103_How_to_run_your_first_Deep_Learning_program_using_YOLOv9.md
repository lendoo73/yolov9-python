# 21-103. How to run your first Deep Learning program using YOLOv9

Object detection on an image:
```shell
python detection.py \
    --weights yolov9-c-converted.onnx \
    --source data/images/horses.jpg
```

Object detection on a video:
```shell
python detection.py \
    --weights yolov9-c-converted.onnx \
    --source data/videos/road.mp4
```

Object detection on webcam:
```shell
python detection.py \
    --weights yolov9-c-converted.onnx \
    --source 0
```

The `yolov9-c-converted.onnx` model is included. Check the model provider's terms before reuse.