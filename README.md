# Penguin Image Dataset

This is a dataset of penguin images used to train the YOLOv5 model. The dataset contains images with penguin targets and provides the corresponding annotation information.

## Structure of Dataset

In this structure, the dataset is organized as follows:

- `data.yaml`: The YAML file holds the root path of the entire dataset and the names of the category and the corresponding numerical labels in the dataset.
- `coco128/`: The root folder of the image data.
    - `images/`: Contains the image data.
        - `train/`: Contains the training images.
            - train1.jpg
            - train2.jpg
            - ...
        - `test/`: Contains the testing images.
            - test1.jpg
            - test2.jpg
            - ...
    - `labels/`: Contains the label files corresponding to the images.
        - `train/`: Contains the label files for the training images.
            - train1.txt
            - train2.txt
            - ...
        - `test/`: Contains the label files for the testing images.
            - test1.txt
            - test2.txt
            - ...

## Data Annotation Format
Each image corresponds to an annotation file, using the YOLOv5 annotation format. Each line represents the annotation information for one target object in the format: **class_id**, **x_center**, **y_center**, **width**, **height**, as follows:
```
2 0.41328125 0.81328125 0.4609375 0.3734375
```

- `class_id`: the class number of the target object.
- `x_center`: x-coordinate of the centre of the target object bounding box, scaled relative to the width of the image.
- `y_center`: y coordinate of the centre of the target object bounding box, scaled with respect to the image height.
- `width`: the width of the target bounding box, scaled relative to the width of the image.
- `height`: the height of the target bounding box, scaled relative to the height of the image.

## Usage Instructions

1. Download or clone this dataset locally.
```bash
git clone https://github.com/Kejia928/local-detection-dataset.git
```

2. When training a model using the YOLOv5 training script, specify the path to the configuration file for the dataset as `data.yaml`