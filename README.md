activate environment 
(base) faryal@faryal-pc:~/Downloads/yolov8/ultralytics/models/yolo/detect$ conda activate yolov10

go to the directory Downloads/yolov8/ultralytics/models/yolo/detect and the run this command for validation on our custom aircraft images 
(yolov10) faryal@faryal-pc:~/Downloads/yolov8/ultralytics/models/yolo/detect$ yolo val model=best.pt data=aircraft.yaml batch=16
