# Breast cancer classification with Keras and Deep Learning

## [The breast cancer histology image dataset](https://www.kaggle.com/paultimothymooney/breast-histopathology-images)

The original dataset consisted of 162 whole mount slide images of Breast Cancer (BCa) specimens scanned at 40x. From that, 277,524 patches of size 50 x 50 were extracted (198,738 IDC negative and 78,786 IDC positive). Each patch’s file name is of the format: uxXyYclassC.png — > example 10253idx5x1351y1101class0.png . Where u is the patient ID (10253idx5), X is the x-coordinate of where this patch was cropped from, Y is the y-coordinate of where this patch was cropped from, and C indicates the class where 0 is non-IDC and 1 is IDC.

![Dataset Sample]("images/breast_cancer_classification_dataset.jpg")


##### Project structure

Clone the repository:
```
git clone git@github.com:walae-br/breast-cancer-classification.git
```

Download the dataset [The breast cancer histology image dataset](https://www.kaggle.com/paultimothymooney/breast-histopathology-images)

create a dataset folder, orig and idc
```
mkdir datasets
mkdir datasets/orig
mkdir datasets/icd
```

Unzip the dataset file into datasets/orig
```
unzip breast-cancer-dataset.zip -x "IDC_regular_ps50_idx5/*"
```

Go ahead and create the training, testing, and validation split directory structure by executing the following command:

```
python build_dataset.py
```

Go ahead and train CancerNet on our breast cancer dataset.

```
python train_model.py
```

![Fig1]("")
