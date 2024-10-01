# LiveHeadCount_YOLO_V3_vs_YOLO_V8

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This project compares the performance of two popular object detection models, YOLOv3 and YOLOv8, for live headcount detection. The goal is to analyze and compare their accuracy, speed, and efficiency in real-time head detection tasks.

### YOLOv3
YOLOv3 is a well-known object detection model that balances detection accuracy and speed. It's robust and can detect multiple objects in a frame with decent precision.

### YOLOv8
YOLOv8 is the latest in the YOLO family, offering state-of-the-art performance with significant improvements in detection accuracy and efficiency. It is designed to outperform previous versions in terms of real-time detection and lightweight deployment.

## Features
- **Real-time headcount detection**: Count the number of heads in live video streams.
- **YOLOv3 and YOLOv8 models**: Compare the performance of these two models.
- **Performance Metrics**: Track speed (frames per second) and detection accuracy.
- **Customizable thresholds**: Fine-tune detection thresholds for better results.

## Installation
1. **Clone the repository**:
    ```bash
    git clone https://github.com/nchirag/LiveHeadCount_YOLO_V3_vs_YOLO_V8.git
    cd LiveHeadCount_YOLO_V3_vs_YOLO_V8
    ```

2. **Set up a virtual environment** (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate   # On Windows, use: venv\Scripts\activate
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Download the pre-trained models**:
    Ensure that you have downloaded the `yolov3.weights` and `yolov8x.pt` files. You can get them from the official YOLO repositories:
    - YOLOv3: [Download weights](https://pjreddie.com/darknet/yolo/)
    - YOLOv8: [Download weights](https://github.com/ultralytics/yolov8)

5. **Set up Git LFS**:
    If you’re handling large files (e.g., model weights):
    ```bash
    git lfs install
    ```

## Usage
To run the live headcount detection and compare YOLOv3 and YOLOv8 models:

1. **For YOLOv3**:
    ```bash
    python detect.py --model yolov3 --weights yolov3.weights --source 0
    ```

2. **For YOLOv8**:
    ```bash
    python detect.py --model yolov8 --weights yolov8x.pt --source 0
    ```

In the above commands, `--source 0` specifies using the webcam. You can replace this with a video file path for testing on a pre-recorded video.

## Results
The results of the detection are compared in terms of:
- **Frames per second (FPS)**: Determines how fast each model processes live frames.
- **Accuracy**: How well each model detects heads in live video streams.
- **Model efficiency**: Resource consumption and processing load.

Graphs and comparisons will be added here once the results are fully evaluated.

## Contributing
Contributions are welcome! Please follow the steps below if you'd like to contribute:
1. Fork the project.
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
