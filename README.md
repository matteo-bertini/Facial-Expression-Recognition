# Facial-Expression-Recognition
In questa repository sono contenuti i vari files del progetto del Laboratorio di Intelligenza Artificiale e Grafica Interattiva.\
L'obiettivo del progetto è quello di esplorare varie reti neurali convoluzionali in grado di effettuare la  Facial Expression Recognition,comparando le loro metriche prestazionali.\
Per eseguire correttamente i file di questa repository è necessario aggiungere al proprio drive questa [cartella](https://drive.google.com/drive/folders/1WnDjOJArsUH-G_ffOXXO7D7dZCs9lLyH?usp=sharing).
La cartella contiene il dataset (il quale può essere scaricato [qui](https://www.kaggle.com/competitions/challenges-in-representation-learning-facial-expression-recognition-challenge/data)) ed i vari modelli allenati delle reti proposte.\
Un esempio descrittivo del dataset (che può essere ottenuto anche nella sezione successiva) è il seguente:
![Images_random_sample](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Exploratory%20Data%20Analysis/eda1.png)

# Exploratory Data Analysis
L'Exploratory Data Analysis è uno strumento essenziale per capire la struttura del dataset e le sue peculiarità(sbilanciamenti fra le classi,valori NaN, ...) e viene implementata dal file `Exploratory_Data_Analysis.ipynb`.\
Una volta eseguito il notebook si ottiene l'istogramma delle classi, grazie al quale si nota subito che il dataset è sbilanciato: 
![classes_histogram](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Exploratory%20Data%20Analysis/eda2.png)\
In particolare si hanno meno immagini di volti appartenenti alla classe "Disgust" , quindi ci si aspetta che le varie reti neurali implementate non saranno in grado di riconoscere la classe efficientemente rispetto alle altre.

# Five-Layers-CNN
La prima rete implementata è una five-layers-cnn,la cui struttura è la seguente:
![flc_struct](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc5.png)\
Una volta allenata la rete,dopo aver adottato alcune tecniche di tuning degli iperparametri si ottengono i seguenti risultati:\ 
train loss: 0.4308 - train accuracy: 0.8481 - val_loss: 0.9865 - val_accuracy: 0.6556 - learning rate: 3.0000e-04
Si può visualizzare la progressione di loss ed accuracy durante la fase di allenamento in modo compatto grazie a questi grafici:\
Loss:\
![loss](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc2.png)\
Accuracy:\
![accuracy](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc1.png)\
Infine,si possono visualizzare in modo compatto le prestazioni della rete comparando le emozioni che predice con le quelle reali dei volti mostrati:
Immagini con emozioni reali:\
![reality](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc3.png)\
Immagini con emozioni predette dalla rete:
![pred](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/Five%20Layers%20CNN/flc4.png)\
Dalle immagini precedenti si notano alcune predzioni errate della rete,ciò è dovuto sia alla sua piccola struttura sia al fatto che alcune emozioni possono essere ambigue ed ogni soggetto le esplicita in modo differente e con sfumature differenti,rendendo il processo di apprendimento più difficoltoso (basta prendere come esempio la figura 4).

# ResNet



