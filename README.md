# Automated-Supermarket-Inventory-Replenishment
Fine Tuning the Yolov5 object detection algorithm to automatically detect and count products kept on supermarket shelves, to make sure all products are replenished.

# Dataset

![collage](https://user-images.githubusercontent.com/63201896/126937855-a686a0ca-c380-49d0-b8ad-bcf6a8961e0e.png)


For this task I had used the SKU110 dataset. It consists of train, validation and test sets. The annotations for the images are provided as a csv file. An example of the csv file is shown below.

![annotations_example](https://user-images.githubusercontent.com/63201896/126936547-9248ea30-2853-48e3-9f65-be2a4c717543.PNG)

* column 1 represents the image name
* columns 2 and 3 represnt the top left coordinates of the bounding boxes.
* columns 4 and 5 represnt the bottom right coordinates of the bounding boxes.
* column 6 represents the class(Since only one class, it is kept as object)
* columns 7 and 8 represent the image widths and heights respectively.


