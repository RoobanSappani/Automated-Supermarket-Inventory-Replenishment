# Automated-Supermarket-Inventory-Replenishment

Fine Tuning the Yolov5 object detection algorithm to automatically detect and count products kept on supermarket shelves, to make sure all products are replenished.

# Dataset

![collage](https://user-images.githubusercontent.com/63201896/126937855-a686a0ca-c380-49d0-b8ad-bcf6a8961e0e.png)

For this task I had used the SKU110 dataset. It consists of train (8232 images), validation (587 images) and test (2940 images) sets. The annotations for the images are provided as a csv file. The number of bounding boxes may vary from image to image. An example of the csv file is shown below.

![annotations_example](https://user-images.githubusercontent.com/63201896/126936547-9248ea30-2853-48e3-9f65-be2a4c717543.PNG)

* column 1 represents the image name.![prediction1](https://user-images.githubusercontent.com/63201896/126940935-4018f536-5baf-4efa-a34e-ea2c4f7d9caf.png)

* columns 2 and 3 represnt the top left coordinates of the bounding boxes.
* columns 4 and 5 represnt the bottom right coordinates of the bounding boxes.
* column 6 represents the class(Since only one class, it is kept as object).
* columns 7 and 8 represent the image widths and heights respectively.

But for the yolo algorithm, we need to change the format accordingly. Roboflow.ai provides a interface where it automatically annotates and augments the iamges accordingly to the yolov5 format. Unfortunately only upto 1000 images can be annotated for free. I used only the resize option(416x416x3) in the preprocessing step. So I used the first 1000 images of the train set and splitted it into train-val-test with a 80-10-10 rule.

# Detection

I used the yolov5s model configurations by only changing the number of classes to 1. Trained the model for 300 epochs and a batch size of 32. The training progress is shown below.

Some of the predictions are shown below.

![observations](https://user-images.githubusercontent.com/63201896/126940121-a1a9c4d1-5a21-4e41-9dd1-4695fdc60990.png)

![prediction2](https://user-images.githubusercontent.com/63201896/126940964-8f530d15-cbcb-40ed-b92b-758bd182743c.png)

![prediction3](https://user-images.githubusercontent.com/63201896/126940979-f0a815e6-9daf-4110-9dfb-ccc36230f2db.png)

![prediction4](https://user-images.githubusercontent.com/63201896/126940991-d333accb-dc2b-496e-ae2a-73895df49531.png)




