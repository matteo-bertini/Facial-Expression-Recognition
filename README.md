

# Introduction

Per eseguire correttamente i file di questa repository è necessario aggiungere al proprio drive questa [cartella](https://drive.google.com/drive/folders/1WnDjOJArsUH-G_ffOXXO7D7dZCs9lLyH?usp=sharing).
La cartella contiene il dataset (il quale può essere scaricato [qui](https://www.kaggle.com/competitions/challenges-in-representation-learning-facial-expression-recognition-challenge/data)) ed i vari modelli allenati delle reti proposte.\

# Exploratory Data Analysis
Exploratory data analysis is an essential tool for analyzing the dataset and understanding its peculiarities.\
Thanks to it, it's possible to grasp important aspects of the dataset such as imbalances between classes, missing values, etc.

The `Exploratory_Data_Analysis.ipynb` file implements the EDA on the dataset, displaying among other things a sample of images and the histogram of the classes, which allows us to understand how these are distributed.

![EDA_image1](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/EDA.png)

In particular, looking at the generated histogram of the classes, it can be seen that the "disgust" class has far fewer images than the other classes, so it will be necessary to do data augmentation to balance the dataset and efficiently train the implemented models.

# Five-Layers-CNN
La prima rete implementata è una five-layers-cnn,la cui struttura è la seguente:
![flc_struct](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc5.png)\
Una volta allenata la rete,dopo aver adottato alcune tecniche di tuning degli iperparametri si ottengono i seguenti risultati: 
train loss: 0.4308 - train accuracy: 0.8481 - val_loss: 0.9865 - val_accuracy: 0.6556 - learning rate: 3.0000e-04.\
Si può visualizzare la progressione di loss ed accuracy durante la fase di allenamento in modo compatto grazie a questi grafici:\
![loss](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc2.png)\
![accuracy](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc1.png)\
Infine,si possono visualizzare in modo compatto le prestazioni della rete comparando le emozioni che predice con le quelle reali dei volti mostrati:
Immagini con emozioni reali:\
![reality](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc3.png)\
Immagini con emozioni predette dalla rete:
![pred](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc4.png)\
Dalle immagini precedenti si notano alcune predizioni errate della rete,ciò è dovuto sia alla sua piccola struttura,sia al fatto che alcune emozioni possono essere ambigue,ed ogni soggetto le esplicita con sfumature differenti,rendendo il processo di apprendimento più difficoltoso (basta prendere come esempio la figura 4).

# ResNet


