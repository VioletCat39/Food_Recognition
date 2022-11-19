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
3. Download this repository to get the resnet18.onnx and Food_Recognition.py to your jetson nano.
4. Open up the Food_Recognition program.
5. You will want to use the downloaded kaggle progarms and sort them into datasets under Food_Recognition: train/Healthy train/Unhealthy, test/Healthy test/Unhealthy, val/Healthy and val/Unhealthy, with an even amount in each dataset. There weren't any direct datasets to train purely on healthy/unhealthy, so it will be required to manually sort the images.
6. Create a labels.txt file with two lines: 1 should be "Healthy", and 2 should be "Unhealthy". 
7. To Re-train the model: Open up the docker container, and run this command to retrain the model:  python3 train.py --model-dir=models/Food_Recognition data/Food_Recognition
8. After it is done training, you may export the model using: python3 onnx_export.py --model-dir=models/Food_Recognition
9. To test this program on any image, exit the docker container, and in the project folder you may run a program with this format: imagenet.py --model=models/Food_Recognition/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/Food_Recognition/labels.txt ImageLocation/Sublocation/image.jpg output.jpg
10. This code can also be used to run the prgram: python3 Food_Recognition.py

Here is a video tutorial with a better example:

https://www.youtube.com/watch?v=RbS2S8ChXfU

      
    
