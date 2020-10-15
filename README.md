# weapon-detection
Handgun, Shotgun and Knife using yolov4-tiny in videos as well as images. Training code, dataset and trained weight file available.

# Dataset
```
  Data is Annotated using Labelme and is available in yolo format with txt files
      ├── data
      │    ├── obj (Train dataset)
      │    │   ├── Knife
      │    │   ├── Handgun
      │    │   └── Shotgun
      │    ├── test (Test dataset)
      │    │   ├── Knife
      │    │   ├── Handgun
      │    │   └── Shotgun
      │    ├── train.txt  (Train label)
      │    └── test.txt   (Test label)
```
[DATASET](https://drive.google.com/drive/folders/1RjYdm1RRnu7htO8jXonHobFUCninJ_TC?usp=sharing)


# Pretrained yolo-tiny weights
[Pre-train model](https://drive.google.com/file/d/1_BBqQ_ZbZkP-AbLjtqsXHPD2i2s_LLdh/view?usp=sharing)


# Colab GPU Training
Complete project is trained and evaluated on google colab
[Notebook](/Train_yolo_tiny.ipynb)


# Knife, Handgun and Shotgun Detection
![predictions](https://user-images.githubusercontent.com/58046531/96093247-8d8e1580-0ee9-11eb-8816-37f060223ae6.jpg "Prediction")

# Important files for Training
```
  Training folder contain important files
      ├── training
      │    ├── obj.data
      │    ├── obj.names
      │    ├── yolov4-tiny.config
      │    └── yolov4-tiny.conv.29  
```

# Training and Prediction command
```
 # train your custom detector! (uncomment %%capture below if you run into memory issues or your Colab is crashing)
 # %%capture
 └── !./darknet detector train training/obj.data training/yolov4-tiny.cfg training/yolov4-tiny.conv.29  -dont_show -map
 
 # run your custom detector with this command (upload an image to your google drive to test, thresh flag sets accuracy that detection must be in order to show it)
 ├── !./darknet detector test training/obj.data training/yolov4-tiny.cfg /mydrive/yolo/yolov4/darknet/backup/yolov4-tiny_4000.weights          /mydrive/yolo/yolov4/darknet/data/test/Knife/7bc500661f0ea2c7.jpg -thresh 0.5
 └── imShow('predictions.jpg')
```

# Convert Model to tfile for android device deloyment
```All instruction and codes available in Given Notebook 
   ├── tflite.ipynb
```

# For Colab GPU Training I Use this awesome repository for setting yolo
[Yolo](https://github.com/AlexeyAB/darknet)
