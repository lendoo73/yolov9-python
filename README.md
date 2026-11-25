# YOLOv9 Object Detection with ONNX Runtime

Run YOLOv9 object detection on images, videos, or a webcam using OpenCV and ONNX Runtime.

## Setup

Use Python 3.10 or later and install the dependencies:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

The repository includes `yolov9-c-converted.onnx`, stored with Git LFS. The upstream
[YOLOv9 v0.1 release](https://github.com/WongKinYiu/yolov9/releases/tag/v0.1) publishes the
same-named `.pt` checkpoint; the exact lineage of this ONNX file is not recorded locally.
See the upstream [GPL-3.0 license](https://github.com/WongKinYiu/yolov9/blob/main/LICENSE.md)
and model release terms before reuse.

## Run

```powershell
python detection.py --weights .\yolov9-c-converted.onnx --source data\images\zidane.jpg
python detection.py --weights .\yolov9-c-converted.onnx --source data\videos\road.mp4
python detection.py --weights .\yolov9-c-converted.onnx --source 0
```

Press `q` to stop video or webcam inference. Adjust the confidence and IoU thresholds with `--thresh`
and `--iou-thresh`.

## Files

- `detection.py` runs inference and draws detected boxes.
- `yolov9-c-converted.onnx` is the included ONNX model.
- `data/class.names` contains the model's class labels.
- `data/images/` and `data/videos/` contain sample input media.
- `21-103_How_to_run_your_first_Deep_Learning_program_using_YOLOv9.md` provides the original walkthrough.

Additional model files and local virtual environments are excluded from version control.
