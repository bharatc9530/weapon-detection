# weapon-detection
Pistol, Riffle and Fire detection using yolov4-tiny in videos as well as images. Training code, dataset and trained weight file available.

# Colab Training
complete project with files, dataset and save models etc..


[Drive](https://drive.google.com/drive/folders/1-FWDmdL5FR_cjU2DXG40x6z57hInRm0t?usp=sharing)

# Fire and Gun Detection

![result](https://raw.githubusercontent.com/atulyakumar97/fire-and-gun-detection/master/screenshots/0.jpg "Model Output")

### How to use yolo.py:
```
usage: yolo.py [-h] [--webcam WEBCAM] [--play_video PLAY_VIDEO]
               [--image IMAGE] [--video_path VIDEO_PATH]
               [--image_path IMAGE_PATH] [--verbose VERBOSE]

optional arguments:
  -h, --help            show this help message and exit
  --webcam WEBCAM       True/False
  --play_video PLAY_VIDEO
                        Tue/False
  --image IMAGE         Tue/False
  --video_path VIDEO_PATH
                        Path of video file
  --image_path IMAGE_PATH
                        Path of image to detect objects
  --verbose VERBOSE     To print statements
```

### Move inside the project folder and use the following command:
```
python yolo.py --play_video True --video_path videos/fire1.mp4
```

[Dataset](https://www.kaggle.com/atulyakumar98/fire-and-gun-dataset)
