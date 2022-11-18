# Food_Recognition
This is the repository for a program I call Healthy vs Unhealthy, in which the Artificial intelligence program in trained on various libraries of food images grouped by healthiness. For simplicity when coding, I had only included a limitted number of images for each folder, however, there will be links to some Kaggle datasets of images I used for training. The goal of this project is to help people determine what are healthy foods to eat, and what foods would be unhealthy.


## The Algorithm
This code takes in different image datasets catagorized manually into healthy vs unhealthy foods. It then takes in these images and trains on similarities in the foods presented, and it can come out with an output for if it thinks a particular image shows healthy or unhealthy food. This program is based off of imagenet, and can recognize one image at a time. 

## Running This Project
There are a few crucial steps for making sure this program works.
1. Make sure you have Visual Studio Code downloaded to your computer/laptop, and make sure it is "SSH"ed into your nano.
2. You may download these datasets off of Kaggle, or you can download and create your own dataset if you choose (Although it will take longer tp compile and sort):
https://www.kaggle.com/datasets/shivanir23/sample-fruitsveg
https://www.kaggle.com/datasets/kmader/food41
https://www.kaggle.com/datasets/cristeaioan/ffml-dataset
3. Download resnet18.onnx and Food_Recognition.py to your jetson nano.
4. You can use python3 Food_Recognition.py to run this program. 

