
# Experiments on Fabric and Nike Shoe logo Dataset

 - Fabrc data and Nike Shoe logo is a binary class dataset provided by IBM to experiment on our model
 - We used our Fenet Model on the given dataset by modifying preparedataloader.py file. 
 - Major issue was with the number of workers in dataloader module. We had to change it to less than 4 because the data is stored in csv files and inside csvs we have location of the images. So jumping from one file to another file is a challenging task for number of workers and the data is also less so if we had more workers then many workers will go out of data. So with less workers each worker will get equal data and take there time to go from one file to another.
 - When the pipeline was prepared the training was done on "raw_images_twoclass_train" images and found out the accuracy of train to reach 99 percent in the fifth epoch onwards.
 - The testing accuracy was calculated on three different datasets, Test, Val and unseen datasets.
 - The result came out to be exceptional with accuracy reaching to 100 percent in less than 5 epochs for test and val images and for unseen it took 26 epochs.
 - Next the dataset provided was of Jan 20 with same test, val and unseen and we reached 100 %test accuracies in less than 5 epochs.
 - Accuracy curve and confusion matrix was plotted for the given accuracies .



## Required Python Dependencies

To run the code, Install the dependencies first using the following commands

```bash
  pip3 install pillow==8.2.0
  pip3 install torch==1.7.1
  pip3 install torchvision==0.8.2
  pip3 install torch-encoding==1.2.2b20200808
  pip3 install mlflow
  pip3 install barbar
  pip3 install Ninja
  pip3 install matplotlib
```


## Dataset Directory

To run the code, configuration file is important which can be accessed in main.py by following code

```bash
  fname = "../../config/binary_classifier_config.json" (Location of the config file)
  cfg = json.load(open(fname, 'r'))
```
Datasets can be accessed through the following directories

```bash
 "train": "../datasets/CSVs/new_rawimages_jan20_two_class_train.csv", 
 "val": "../datasets/CSVs/new_rawimages_jan20_two_class_val.csv",
 "test": "../datasets/CSVs/new_rawimages_jan20_two_class_test.csv",
 "unseen": "../datasets/CSVs/new_rawimages_jan20_two_class_unseen.csv",
 "unseen_jan10": "../datasets/CSVs/new_rawimages_two_class_unseen.csv"},
```

## Code Run

Run the code using following command on colab or terminal


For Fabric dataset
```bash
  python main.py --n_classes=2 --train_need --test_need  --test_BS=16 --train_BS=8  --model=FENet --use_pretrained --num_epochs=30 --scheduler="cosine" --lr=0.001 --num_workers=0
```
 For Nike Shoe Logo dataset
```bash
  python main.py --n_classes=2 --train_need --test_need  --test_BS=16 --train_BS=8  --model=FENet --use_pretrained --num_epochs=30 --scheduler="cosine" --lr=0.001 --num_workers=0
```   
## Demo

Insert gif or link to demo


## Deployment

To deploy this project run

```bash
  npm run deploy
```


## Dataset Images

- Image of Authentic data

![Image of Authentic data](https://github.com/faisu07/Fbric-Experimentation/blob/main/real.jpg)

- Image of Counterfeit data

![Image of Counterfeit data](https://github.com/faisu07/Fbric-Experimentation/blob/main/counterfeit.jpg)


## Trainining Curve 

- Training curve of fabric data

![Training curve of fabric data](https://github.com/faisu07/Fbric-Experimentation/blob/main/Accuracy_fabric_val.png)

- Training curve of Nike data

![Training curve of Nike Show Logo data](https://github.com/faisu07/Fbric-Experimentation/blob/main/Accuracy_nike_val.png)

## Confusion Matrix  (Test,Val,Unseen in order)

- Fabric Data

![Confusion matrix of fabric data test](https://github.com/faisu07/Fbric-Experimentation/blob/main/cm_test.png)

![Confusion matrix of fabric data val](https://github.com/faisu07/Fbric-Experimentation/blob/main/cm_val.png)

![Confusion matrix of fabric data unseen](https://github.com/faisu07/Fbric-Experimentation/blob/main/cm_unseen.png)


- Nike Show Logo Data

![Confusion matrix of Nike data test](https://github.com/faisu07/Fbric-Experimentation/blob/main/Confusion_test.png)

![Confusion matrix of Nike data val](https://github.com/faisu07/Fbric-Experimentation/blob/main/Confusion_val.png)

![Confusion matrix of Nike data unseen](https://github.com/faisu07/Fbric-Experimentation/blob/main/Confusion_unseen.png)



## Authors

- [@Vijay Pandey](https://www.linkedin.com/in/vijay-pandey-29a0a35a)
- [@Mohammed Faisal](www.linkedin.com/in/mohammed-faisal-771b8818b)
- [@Mayank Gubba](https://www.linkedin.com/in/mayank-gubba/)


## Appendix

Any additional information goes here

