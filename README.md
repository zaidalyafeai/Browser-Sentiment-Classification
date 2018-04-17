# Browser-Sentiment-Classification

## Project Description 

* NLP Sentiment Analysis.ipynb creates the model and trains it on the texts from the 'sentiment.txt' file. In order to make things easier for the browser app we cache the dictionary which maps the words to indices inside dict.csv. The trained model is then saved into keras.h5 file.

* After that you convert the trained keras model into a model.json file in order to load it in the browser. The conversion is done using the command 

`tensorflowjs_converter --input_format keras keras.h5 output/`

* The output foulder will then contain one model.json file and 5 group* files which contains the saved weights of the model. These weights are referenced using variables from the json file 

* The testRNN.html file loads the json file and creates the trained model. The use it to predict texts. 
