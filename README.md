## activate environment 
`
(base) faryal@faryal-pc:~/Downloads/yolov8/ultralytics/models/yolo/detect$ conda activate yolov10`

## Train
go to the directory Downloads/yolov8/ultralytics/models/yolo/detect and run


` $ yolo detect train data=aircraft.yaml model=yolov8s.yaml epochs=100  batch=16  imgsz=416 device=0,1`

## Val
go to the directory Downloads/yolov8/ultralytics/models/yolo/detect and the run this command for validation on our custom aircraft images 


` $ yolo val model=best.pt data=aircraft.yaml batch=16`

![P_curve](https://github.com/user-attachments/assets/7584c57b-d0c3-488c-a2e8-b03fab663cd1)
![PR_curve](https://github.com/user-attachments/assets/51556639-2c00-4e9b-b096-06e1a94fae6d)
![R_curve](https://github.com/user-attachments/assets/63403d2b-23f3-49b9-b592-f29c4fce3019)
              Class     Images  Instances      Box(P          R      mAP50  m
                   all       1150       4618       0.28       0.68      0.452      0.357
                  F_16       1150       1117      0.215      0.798      0.401      0.322
                  F_35       1150        875      0.269      0.253      0.401      0.308
                 SU_27       1150       1101      0.272      0.775      0.447      0.358
                    WB       1150        171      0.171      0.936      0.517      0.446
                 Other       1150        322      0.447      0.624      0.555      0.404
                   A10       1150        281      0.336       0.16      0.274      0.209
                  F_15       1150        166      0.195       0.97      0.576       0.44
                  Pens       1150         35      0.371      0.686      0.445      0.365
                  Ammo       1150        550      0.244      0.916      0.455      0.362
Speed: 0.2ms preprocess, 2.2ms inference, 0.0ms loss, 0.1ms postprocess per image
results are not as good as with yolov10

## Predict
Inside the directory Downloads/yolov8/ultralytics/models/yolo/detect, run the command 

`$ yolo predict model=best.pt source=output/test/images `
