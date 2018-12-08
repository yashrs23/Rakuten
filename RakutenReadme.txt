Rakuten Deep Learning Challenge

I started the challenge with some analysis of data. The data was huge. There were around 554656 images which we can use for training our classifier and 118864 were given on which we need to test our model.  I started to train my model with resnet34 with imagenet pretrained weights. Just last layers were changed and the model was trained on the dataset. Then I unfreezed all the layers of the model and train the model with discriminative learning rate. 

For prediction I first find out the probabilities of all 43 classes. Then all the probabilities were sorted in descending order and I took top three out of them. Our objective was to predict top 3 classes for each image in test folder. So those probability values are mapped to their respective classes. 

I also tried resnet50 and resnet101 later on. Both of these gave better results than resnet34. First I trained resnet50 in a similar way like I trained resnet34 and got better results. Similarly when resnet101 was trained, it initially coverged very well. Due to limited computing resources I felt restricted in resnet100. Time taken for each epoch in resnet100 was much higher than the other two. But complex structure of resnet 100 helped me. Patience with resnet100 gave best results. It feels like deeper neural networks are really working good on dataset.

I have used pytorch 1.0 and fastai 1.0 framework for the problem

