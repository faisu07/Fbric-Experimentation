
# Experiments on Fabric and Nike Shoe logo Dataset




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



## Documentation


## Authors

- [@Vijay Pandey](https://www.linkedin.com/in/vijay-pandey-29a0a35a)
- [@Mohammed Faisal](www.linkedin.com/in/mohammed-faisal-771b8818b)
- [@Mayank Gubba](https://www.linkedin.com/in/mayank-gubba/)


## Appendix

Any additional information goes here

