# three-letter-mnist
Handwritten Character Disentanglement Benchmark compiled from EMNIST dataset

EMNIST Letters data set modified to create 3-letter words.  List of 100 commonly occuring 3 letter words is included in top_words.txt

read_data checks if data set is available in this repository, and, if not, downloads, unzips, and prepares the data set.  It is called as the 'main' method.  

Specify # of samples of each word to include in the data set (per_word = 600 is default, and results in 600*100 words = 60000 samples).  'read_data' thus returns a numpy array of size (per_word*num_words, 28*84).  Reshape into a 28 x 84 image for viewing with 'show'.  

Each sample is generated by randomly choosing an image for each letter in the word.  Specify a seed to reproduce given data set.  Set save_img = True (likely with low per_word to avoid too many duplicates) to save test images to a new 'examples' folder.  

