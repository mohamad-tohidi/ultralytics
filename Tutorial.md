1. Losses 
    we have three losses in YOLO
    1. dfl : its for determining the width and height of the bbox
    2. box : its for detectign the center of the bbox
    3. cls : for prediciting the class of the object

    by changing the cls, and dfl, and box values we can controll the models focus on specific problem

    ```
    yolo train data=coco8.yaml model=yolo11n.pt cls=1.0 box=7.5 dfl=1.5 
    ```


2. Augmentations
    ultralytics applies online Augmentations
    we should check them, and disable them if they are harmfull for our dataset

    **NOTE**: augmentation, is for making the model robust to different scenarios
    and not for generating lots of data.

    ```
    yolo train data=... mosaic=0 
    ```

TODO: create a test dataset for testing the tricks

3. 