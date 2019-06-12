# img-classifier-ships
A simple classifier using transfer learning with EfficientNet by Google

This simple script use a Dataset of over 8000 images of ships from https://www.analyticsvidhya.com/ (Games of Deep Learning Competition)

Images were previously resized to make them homogeneus, then a KFold procedure was used to validate my model (K = 5 with the same distribution per class)
Data were augmented to enlarge the train dataset.
Transfer learning was done using EfficientNetB3 by Google* and AdaBound** optimizer
I used a Customize loss function which try to minimize F1 score (the metric used for this competition)
After 80 epochs on the whole training set I reached 0.96 F1 weighted score on the test set (about 2800 images). Better results could be achived with more epochs (validation
loss was still decreasing after 80 epochs).

* https://arxiv.org/abs/1905.11946
** https://arxiv.org/abs/1902.09843
