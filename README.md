# Next_word_predictor-indic-language-
Using a telugu language corpus to predict the next word with the help of nltk library  

• This report is in regards to the WORD PREDICTOR model made using an Indic corpus.  
• The Indic corpus contains 6100 sentences and 75151 words in TELUGU LANGUAGE.  

APPROACH:    

We start out with an Indic corpus of Telugu language with 47 million sentences and close to 500 million words. But due to computing restriction, the corpus was downsized.  

The approach to read the corpus and make models was done using NLTK library. The corpus was imported to be read as a string.  
Then the text was normalized to convert every ‘.’, ‘,’, ‘:’ into a ‘ ‘ for separating the sentences.  
The sentences then were split using segmentation with the split function for splitting the string form in which the corpus was read.  
The corpus is then split using the split function on the sentences obtained. Next, the number of tokens are counted and the frequency is given.  

The heaps law is verified using the tokens and the number of unique tokens and a plot is created for unique tokens and total number of tokens.  
Number of distinct unigrams is calculated which is infact equal to the number of unique tokens in the corpus.  
The ZIPF’s law is verified using the tokens from the corpus. After that the most common tokens that follow each other are calculated with the frequency they occur at
(in which the times a ‘.’ follows a ‘.’ Is the most which occurs 251 times in the corpus).  

Now, the bigram and trigram libraries are imported from nltk.collocations and nltk.metrics .  
The number of unique bigram models are then counted, which are stored in a bigram_corpus variable and displayed which is 68535.  
The bigrams are all displayed next including the frequency they appear at with the plot of their frequency.  
The trigrams are stored in a variable trigram_cmn displayed with their frequencies and the then the number of unique trigrams are calculated which is 72401 in number.  
The number of 4-gram models are found out next from the tokens of the corpus. Unique 4-gram models in the corpus are 72709.  
Similarly, the 5-gram models are found out and the number of unique 5-gram models was found out to be 72775.  

The unigram models are calculated with 2 given inputs using the above created unigram list which contains all possible unigrams.  
Similarly bigram and trigram models are calculated with given inputs from the corpus.  
NOW, we attempt to create a LANGUAGE MODEL for predicting the next word.  

The working of this is based on the following: -    
• Interpolation is used instead of Laplace smoothing for better results.    
• The best 3 words are predicted based on unigram, bigram and trigram model.  
• The probability is given by P=P1*λ1 +P2*λ2 +P3*λ3 where λ1 is 0.1, λ2=0.4 and λ3=0.5  


The desired outputs are then calculated when the inputs are given from the corpus.  
Hence, we have successfully predicted the next 3 words based on unigram, bigram and trigram models.  

