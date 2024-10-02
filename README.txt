Readme File

Contents of Zip File: 
0. Readme File.
1. Part 1 : Data cleaning, preprocessing, tokenization, standardization, lyrics length , Lemmatization, POS tagging, Word Frequency, Most common Word, Sentiment Analysis.
2. Part 2 : Sentiment Analysis.
3. Dataset 1: Mainly used for Part 1 and for Part 2.
4. Dataset 2: Used to increase the accuracy of the model in Part 2, preditive model.
5. Presentation Slides: The final presentation of the project. 



Part 1: 
- We have imported the dataset and have dislayed a sample fo the dataset.
- We have tokenized the one single lyrics and have inspected any abnormalities during the tokenization, to rectify it in further process.
- We have tokenized the lyrics and removed unwanted inclusions in the tokenization step, we have then insterted this new tokenized entry into a column called tokenized lyrics.
- We created three new columns namely for Lyrics length, standardized lyrics length and average lyrics length respectively. In this step we have added the lyrics length of each of the songs, standardized the lyrics length and finally calculated the average lyrics length for an artist considering all his/her songs in the datset.
- We have displayed the top 10 artists with highest average lyrics length and the bottom 10 artists as well.
- Plot of the average lyrics length of artists



Part 2: 
-This folder contains 2 datasets and the predictive models ran on both.
-The first dataset is one csv file that contains 745 songs made by 21 different artists.
-The second dataset contains 21 artists but we scrapped BTS since they are not exclusively english.
-We also scrapped 8 other artists that had the least amount of songs in their csv since we wanted
to see the model trained on a lot of data. We also wanted to keep the songs per artist consistant in our model.
-This left us with 12 artists each having 296 songs in the dataset. Both models are using a neural network with the following structure: 
-Dense Layer with 100 outputs, relu activation, and a 25% dropout -> Dense Layer with 50 outputs, relu activation, and a 25% dropout -> Dense layer with 21/12 targets, softmax activation. Both models
use ADAM with a learning rate of 1e-4 and a cross entropy loss function. The dropout layers were included toincrease our validation accuracy.
-With both datasets during training, we use a batch size of 70 along with having
1/4 of the data be for validation. 
-Both models preform almost perfect on the training data and the first and second model have an accuracy of 29% and 68% respectively. 
-Since the first model has 21 targets compared to 12 we wanted to see how much better each model does compared to a random guess.
-We found that the first model has a 6.09x better chance of guessing the correct artist while the second model has a 7.92x better chance of guessing the correct artist.


Challanges:
1. Procuring dataset that is large enough for predictive modeling: As the predicitve modeling gets better with larger amounts of data, one challange we faced was to provide the model with large enough dataset for processing. 
2. Ambiguity of words used in the lyrics for POS Tagging: As the POS tagging works on words in english and there are times when it can not properly differentiate between the words to give it the correct POS. 
3. Some jargons could not be detected during lemmatization: Some jargons that would mean something else could not be converted completely during lemmatization, thats something we could consider in future scope of work. 
4. Words used in different languages: As there were many songs that had words used in different languages it was not possible to inlucde such words in the most common words counter as these words would not match with most other songs that were in english.


Limitations: 
1. Limited Data: As mentioned above, with extensive data the modle could give better predictions.
2. Limited Attributes to work on: We only had 3 columns that we could work on, with more attributes like date, time, ranking etc the model would be in a better position to arrive at predictions that before. 