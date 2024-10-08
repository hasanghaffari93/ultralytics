| Argument      | Type    | Default | Description                                                                                                                                                 |
| ------------- | ------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `data`        | `str`   | `None`  | Specifies the path to the dataset configuration file (e.g., `coco8.yaml`). This file includes paths to validation data, class names, and number of classes. |
| `imgsz`       | `int`   | `640`   | Defines the size of input images. All images are resized to this dimension before processing.                                                               |
| `batch`       | `int`   | `16`    | Sets the number of images per batch. Use `-1` for AutoBatch, which automatically adjusts based on GPU memory availability.                                  |
| `save_json`   | `bool`  | `False` | If `True`, saves the results to a JSON file for further analysis or integration with other tools.                                                           |
| `save_hybrid` | `bool`  | `False` | If `True`, saves a hybrid version of labels that combines original annotations with additional model predictions.                                           |
| `conf`        | `float` | `0.001` | Sets the minimum confidence threshold for detections. Detections with confidence below this threshold are discarded.                                        |
| `iou`         | `float` | `0.6`   | Sets the Intersection Over Union (IoU) threshold for Non-Maximum Suppression (NMS). Helps in reducing duplicate detections.                                 |
| `max_det`     | `int`   | `300`   | Limits the maximum number of detections per image. Useful in dense scenes to prevent excessive detections.                                                  |
| `half`        | `bool`  | `True`  | Enables half-precision (FP16) computation, reducing memory usage and potentially increasing speed with minimal impact on accuracy.                          |
| `device`      | `str`   | `None`  | Specifies the device for validation (`cpu`, `cuda:0`, etc.). Allows flexibility in utilizing CPU or GPU resources.                                          |
| `dnn`         | `bool`  | `False` | If `True`, uses the OpenCV DNN module for ONNX model inference, offering an alternative to PyTorch inference methods.                                       |
| `plots`       | `bool`  | `False` | When set to `True`, generates and saves plots of predictions versus ground truth for visual evaluation of the model's performance.                          |
| `rect`        | `bool`  | `False` | If `True`, uses rectangular inference for batching, reducing padding and potentially increasing speed and efficiency.                                       |
| `split`       | `str`   | `val`   | Determines the dataset split to use for validation (`val`, `test`, or `train`). Allows flexibility in choosing the data segment for performance evaluation. |
