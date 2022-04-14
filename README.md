# 2017ISIC_EPQ

The code for my EPQ project, focused on achieving a good accuracy on the ISIC 2017 challenge task 3 https://challenge.isic-archive.com/landing/2017/44/.
82% accuracy was achieved on the unseen test set and a score of 0.93 on the mean AUC ROC. Only the datasets provided by the 2017 challenge were used.

<img width="441" alt="image" src="https://user-images.githubusercontent.com/22745975/163481134-83d016c9-397a-4183-bdbd-31eebe30ddb0.png">
AUC ROC is used in binary classifiers. Task 1 is melanoma classfication, task 2 is seborreic keratosis classification.

5 diffrents models were trained (4 ConvNeXt-L and 1 Swin-B, both pretrained) for 200 epochs, however the models were saved earlier to due to the early stopping policy.
Models were trained with a few simple transformations and mixup. Adam optimizer was used alongside a one cycle learning rate scheduler. 
The ensemble model was trained for 10 epochs using Adam and a constant learning rate.

Further improvement: 
I finished this project several months ago (first thing I did after finishing my deep learning nanodegree). 
In this time that has passed my knowledge deepend. 

If I were to do this again now I would:

1. The model architecture was overkill, a smaller one would be more appropiate

2. Dataset size would be expanded, and classes would be balanced

3. Folds would be used for the ensemble

4. Other transformations would also be used 
