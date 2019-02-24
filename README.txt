----------------------------------------------
COS 424: Sentiment Analysis Task (Spring 2019)
----------------------------------------------

This directory comprises the following files

- data/train.txt, a training set of 2400 sentiment labelled sentences 
(from Amazon, Yelp and iMDB) in the following form:
<sample num>	<sentence> 	<sentiment> 
where <sentiment> is either 0 (negative) or 1 (positive).

- data/test.txt, a test set of 600 labelled sentences, in the same format.

- preprocessSentences.py, called as follows: 
	python ./preprocessSentences.py -p <data> -o <out> -v <vocab>
<data> is the path of the directory containing train.txt,
<out> is an optional argument specifying the prefix of output files, and 
<vocab> is an optional argument specifying the path to an existing 
vocabulary file.

- The initial preprocessSentences.py script has been written for the 
version 2 of Python. preprocessSentences_v3.py is the script compatible
for the version 3.

The script generates four output files in <data>: 
	- A vocabulary file 'out_vocab_*.txtâ€™ (if one is not specified 
when calling the script) with tokenized words from the training data 
(where '*' is the word count threshold, set to default as 5 in the 
script), 
	- A list of training samples numbers in 
'out_samples_classes_*.txt',
	- A list of sentiment labels corresponding to each training 
sample, 'out_classes_*.txt', and
	- A 'bag of words' featurized representation of each sentence in 
the training set, 'out_bag_of_words_*.csv'

----------------------------------------------
