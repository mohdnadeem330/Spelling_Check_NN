# Spelling_Check_NN
Neural Network to spell check word for english language. For instance "wrk" should return "work" as the closest match.
Neural network model to check spellings
Using the latest tensorflow modules the aim of this project is to check spellings of words.
We have used Attention Decoder in decoding layer and bidirectional recurrent neural network in encoding.

Approach:
Our process is mainly divided into following parts:
1) First we extract the words from data and we clean the text using clean_text function then create functions to convert word to vectors and vice versa after creating a dictionary for it. Also we split sentences as training and testing samples and measure there length.
2) Then we create a function called noise maker to classify noisy sentences. Next we create placeholders for inputs to our model.
3) Now we use the encoding layer functions to encode our words and decoding layer functions to decode them using BadhanuAttention mechanism in seq2seq library of tensorflow.
4) We define the whole process in the seq2seq model. Also each sentence has the same length of words is ensured in another function. Then we ultimately get batches of sentences.
5) Now we define 100 epochs with a batch size of 128 and 2 layers for our recurrent neural network of seq2seq model. We thus train our model.
6) We keep a probability of 0.75, and threshold of 0.95 for our model. We can use our model for customized sentences using another function that converts them into integers and cleans them then runs them on our trained model. 

For Testing:
In the notebook just modify the  text an run the model for your own customized sentences.

Bottleneck:
The results can be better.
