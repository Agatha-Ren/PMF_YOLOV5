# PMF YOLOV5 

### 1) Converting the coco format to Yolov5 format:
```
cd yolov5-master
run coco_converter_yolov5.ipynb
# the path need to be noticed that to offer the json path. 
# put the label file and image in yolov5-master/data/dataset or image in data/image and label in data/label
```

### 2) Randomly split the dataset to train, value and test:
```
cd yolov5-master
run split.ipynb
# please note that the path should be consistent
# can create three files which are train.txt, val.txt and test.txt to store the image name in files.

```

### 3) Train a model (see the parameter settings in the script, including path and batch size ):
```
change the path in PMF_yolov5.yaml
run train.py
# notice that the class number should be changed in the chosen model. eg. in yolov5m.yaml the clase number has changed to 4.
```

### 4) Test the model (see the parameter settings in the script):
```
run detect.py
# notice the parameters of weight and source. the weight path is in the runs/exp.../best.pt. source path should be the test.txt
```
Please refer to `../data/pmf_demo/generated_images/` for the augmented images with prediction and ground truth, and if mask_on=True was set for the training, the same should be done for testing as well):

### 5) Get the result (see the parameter settings in the script):
```
run test.py
# notice the parameters of weight, data and batch size. 
```


