# Ciphar10 using PyTorch

## Build in Your System
```Bash
pip install pytorch sklearn cupy

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
