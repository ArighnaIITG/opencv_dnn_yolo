# Opencv_DNN_YOLO
OpenCV `dnn` module supports running inference on pre-trained deep learning models from popular frameworks like **Caffe, Torch and TensorFlow**.


Support for running YOLO/DarkNet has been added to OpenCV dnn module recently.

## Dependencies

1. OpenCV (`pip install opencv-python`)
2. Numpy (`pip install numpy`)

**Note : Python 2.X is not supported**

## YOLO (You Only Look Once)

YOLO (You Only Look Once) is a method / way to do object detection. It is the algorithm /strategy behind how the code is going to detect objects in the image. The official implementation of this idea is available through [DarkNet](https://pjreddie.com/darknet/) (neural net implementation from the ground up in 'C' from the author).
There are other popular object detection frameworks like **Faster R-CNN** and **SSD** that are also widely used.

Download the pre-trained YOLO v3 weights file from this [link](https://pjreddie.com/media/files/yolov3.weights) and place it in the current directory or you can directly download to the current directory in terminal using :

`$ wget https://pjreddie.com/media/files/yolov3.weights`

Provided all the files are in the current directory, below command will apply object detection on the input image `dog.jpg`.

`$ python yolo_opencv.py --image dog.jpg --config yolov3.cfg --weights yolov3.weights --classes yolov3.txt`

### Command format

The script requires four input arguments.
```
1. input image
2. YOLO config file
3. pre-trained YOLO weights
4. text file containing class names
```

The **format** is like this :

`$ python yolo_opencv.py --image /path/to/input/image --config /path/to/config/file --weights /path/to/weights/file --classes /path/to/classes/file`

## Sample Output

The sample output of the picture will be like this :



