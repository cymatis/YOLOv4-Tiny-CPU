# YOLOv4-Tiny-CPU 
## MSCOCO Performance Comparison   
Model was trained by using MSCOCO trainval 2017 datasets and tested with OpenCV Deep learning module.   
mAP was calculated from the codaLab competition with MSCOCO testdev2019.   
YOLOv4-Tiny-CPU used the anchor values calculated on MSCOCO train data.     
Name of CPU indicates the FPS on the device.   
vCPU used Google Compute Engine with N2 High CPU Machine type. (Intel Cascade Lake)
| Model | Size | AP<sub>50</sub> | BFLOPs | Model size |
|:-------------------|--------:|--------:|--------:|--------:|   
| [YOLOv4-Tiny](https://github.com/AlexeyAB/darknet "Alexey") | 416 | 40.2 | 6.9 | 23.1MB |
| [YOLOv4-Tiny-CPU](https://drive.google.com/file/d/11gbL1hE9IuXxsvblE91Ui4Q-1zHuULIf/view?usp=sharing) | 416 | 40.2 | 5.4 | 15.7MB |    

| Model | vCPU x2 | vCPU x4 | vCPU x8 | i7-10700 | i7-9700K | i7-6850K | i5-8265U | ARM A52 |
|:-------------------|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|
| [YOLOv4-Tiny](https://github.com/AlexeyAB/darknet "Alexey") | 2.52 | 5.07 | 10.11 | 56.6 | 31.7 | 19.8 | 8.4 | 0.98 |
| [YOLOv4-Tiny-CPU](https://drive.google.com/file/d/11gbL1hE9IuXxsvblE91Ui4Q-1zHuULIf/view?usp=sharing) | 3.05 | 6.10 | 12.45 | 61.6 | 40.3 | 25.8 | 11.3 | 1.33 |


## Test on video
https://github.com/opencv/opencv/blob/master/samples/dnn/object_detection.py

```
python3 object_detection.py --config=cfg/yolov4-tiny-cpu.cfg --model=weights/yolov4-tiny-cpu.weights --classes=coco.names --width=416 --height=416 --scale=0.00392 --input=test.mp4 --rgb
```

