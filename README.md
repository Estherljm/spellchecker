# Overview 
There are 3 main parts to this project: 

1. Dictionary formulation 
2. Spell checking formulation 
3. GUI formulation 

## Dictionary Formulation 
This part involves creating a unigram, bigram and trigram dictionary based on the corpus used. Each dictionary were used for different purposes in the spell checking process. 

## Spell Checking Formulation 
This spell checking system was built to correct real word and non-word errors. 

**Non-word error** - Tokenize inputs and compare them with the unigram dictionary created. If the token **does not** exist in the dictionary, it is a non-word error. 
A list of candidate words are suggested according to the cost of **edit distance** and unigram probability.  

**Real word error** - Tokenize inputs and compare them with the unigram dictionary created. If the token **does** exist in the dictionary, **Stupid Backoff Method** is used to get a list of potential real word errors.
The candidate words are then filtered based on the cost of edit distance and probability score.

## GUI Formulation 
![alt text](https://github.com/Estherljm/spellchecker/blob/master/img1.png)
- Text box can accept input text of up to 500 words 
- Non-word error highlighted in red, real word error highlighted in blue 
- Right click on errors to get a pop up of suggested words 
- Right side of the GUI allows user to search for words in the dictionary 
