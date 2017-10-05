# LSTMCharGen
This is a repository for my LSTM Character Generator. It is based on Chun ML https://github.com/ChunML/text-generator, which I believe is based on Andrej Karpathy's original work.

# What this program does
This program generates new text based on its learning of existing text within an LSTM neural network. It generates the new text character by character (NOT word by word). It randomly picks a starting chracter and then generates from that point, using the predicted chracter as the base for the next generated character. For example:

The model chooses 'a' as the first chracter, it then predicts what the next character will be by choosing the most probable character based on its learned text. So lets just say the model predicts 's' as the most probably next character. It then runs another predict and uses 'as' as the chracters to predict from next. Lets say the model chooses 'k' as the next most probable character. We now have started to construct our sentence and we have the word 'ask'.

It will continue to do this task for the number of iterations that we tell it to. 

Please keep in mind that ' ' (blank spaces) '.' (punctuation) also count as chracters in this model so it can also make spaces and punctuate sentences as they should be and as whatever style source material you used to train the model is written in.

# What this program code requires
Not too much just:

Python, 
Numpy, 
Keras, 
Argparse, 
Time, 
Csv, 
Matplotlib, 

# Where do we go from here
Next step with this model I believe is to try and add some more different layers to the LSTM. I believe that a dropout layer might help improve the learning. 

Also we could investigate if it is possible to add in some sort of 'nudge' to get it to predict certain letters more often than it does based on learning from the base text. For example can we adjust the weights so that it predicts the next character to be 's' given it is predicting from 'a'.

Moving on from this model I am working to build up a word generator. It should be structured quite similar to this chracter generator but some slight modifications to made it predict words. I believe this will help with the issue of coherancy of text generated just for the simple fact that undertanding a sentence based on words should be better than one simply based on characters.
