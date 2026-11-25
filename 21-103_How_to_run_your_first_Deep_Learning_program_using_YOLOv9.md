# 21-103. How to run your first Deep Learning program using YOLOv9

Object detection on an image:
```shell
python detection.py \
    --weights path/to/model.onnx \
    --source data/images/horses.jpg
```

Object detection on a video:
```shell
python detection.py \
    --weights path/to/model.onnx \
    --source data/videos/road.mp4
```

Object detection on webcam:
```shell
python detection.py \
    --weights path/to/model.onnx \
    --source 0
```

Model weights are not included in this repository. Supply a compatible YOLOv9 ONNX model using
`--weights`, and follow the model provider's terms.