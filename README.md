## activate environment 
`
(base) faryal@faryal-pc:~/Downloads/yolov8/ultralytics/models/yolo/detect$ conda activate yolov10`

## Train
go to the directory Downloads/yolov8/ultralytics/models/yolo/detect and run


` $ yolo detect train data=aircraft.yaml model=yolov8s.yaml epochs=100  batch=16  imgsz=416 device=0,1`![F1_curve](https://github.com/user-attachments/assets/68caf3a1-362c-4ad6-bf8d-c00c2c551a58)


## Val
go to the directory Downloads/yolov8/ultralytics/models/yolo/detect and the run this command for validation on our custom aircraft images 


` $ yolo val model=best.pt data=aircraft.yaml batch=16`



![PR_curve](https://github.com/user-attachments/assets/003f5297-c4d2-46ae-8f41-8a914c46e144)
![P_curve](https://github.com/user-attachments/assets/bce4d5ba-070b-4ea5-b25a-a34078d143f6)
![R_curve](https://github.com/user-attachments/assets/8aa1279b-7941-49a0-acb6-30877b5f9847)



## Predict

Inside the directory Downloads/yolov8/ultralytics/models/yolo/detect, run the command 

`$ yolo predict model=best.pt source=output/test/images `
