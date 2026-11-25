# YOLOv9 Object Detection with ONNX Runtime

Run YOLOv9 object detection on images, videos, or a webcam using OpenCV and ONNX Runtime.

## Setup

Use Python 3.10 or later and install the dependencies:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Provide a compatible YOLOv9 ONNX model separately. Model weights are not included in this repository.
Pass its local path with `--weights`.

## Run

```powershell
python detection.py --weights .\path\to\model.onnx --source data\images\zidane.jpg
python detection.py --weights .\path\to\model.onnx --source data\videos\road.mp4
python detection.py --weights .\path\to\model.onnx --source 0
```

Press `q` to stop video or webcam inference. Adjust the confidence and IoU thresholds with `--thresh`
and `--iou-thresh`.

## Files

- `detection.py` runs inference and draws detected boxes.
- `data/class.names` contains the model's class labels.
- `data/images/` and `data/videos/` contain sample input media.
- `21-103_How_to_run_your_first_Deep_Learning_program_using_YOLOv9.md` provides the original walkthrough.

Model files and local virtual environments are excluded from version control. Check the model provider's
terms before downloading or using model weights.
