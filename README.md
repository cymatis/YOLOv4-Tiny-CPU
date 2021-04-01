# YOLOv4-Tiny-CPU 
## MSCOCO Performance Comparison   
Model was trained by using MSCOCO trainval 2017 datasets and inferenced with OpenCV Deep learning module.   
mAP was calculated from the codaLab competition with MSCOCO testdev2019.   
YOLOv4-Tiny-CPU used the anchor values calculated for MSCOCO train data.     
Name of CPU indicate the FPS on the device.   
| Model | Size | AP<sub>50</sub> | i7-10700 | i7-9700K | i7-6850K | i5-8265U | ARM A52 | BFLOPs | Model size | Pre-trained |
|:-------------------|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|
| [YOLOv3-Tiny](https://pjreddie.com/darknet/yolo "pjreddie") | 416 | 33.1 | 61.8 | - | - | - | 1.10 | 5.6 | 33.8MB | - |
| [YOLOv4-Tiny](https://github.com/AlexeyAB/darknet "Alexey") | 416 | 40.2 | 56.6 | 31.7 | 19.8 | 8.4 | 0.98 | 6.9 | 23.1MB | - |
| YOLOv4-Tiny-CPU | 416 | 40.0 | 61.6 | 40.3 | 25.8 | 11.3 | 1.33 | 5.4 | 15.7MB | [weights](https://drive.google.com/file/d/11gbL1hE9IuXxsvblE91Ui4Q-1zHuULIf/view?usp=sharing)|
