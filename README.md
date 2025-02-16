# Ciphar10 using PyTorch

## Build in Your System
```Bash
# Get PyTorch for CUDA 12.X
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126

# Rest
pip install scikit-learn pandas matplotlib cupy torchsummary

# The Dataset
kaggle competitions download -c cifar-10
```

<hr>
Currently the model weighs at 16mb, using approx. 2M parameters but still produces only 76% accuracy on the Train dataset. Upon uploading to Kaggle this only gives a *score of 0.65*. Help me increase it! 
I have tried K-Fold Cross Validation for 5 folds, and running it for 30 epochs. But it doesn't pass the 80% accuracy at all. The following Data Augmentation tricks have been used:-

* Random Flipping
* Random Scaling
* Color Distortion
* and some more.

The entire model is built to train on the gpu, so u can immediately run it, and it will run directly on the gpu!

<hr>  

## New Updates!!!      
Lowered the Model weight to just **4mb!!!** While increasing the base accuracy to **85%!!!**
You can load the saved `model_fold_5.pth` to use the model! 

I tried to include the testing data that has 300,000 images with the train data. 
Implemented Semi-Supervised Learning by predicting the outputs of the testing data and only considering the one's that have over 95% predictive accuracy.
Included these into the training data and re-trained the model with 4 fold cross validation which gave a **97% accuracy!!!**
You can load the `retrained_model_fold_4.pth` model to use it!      
