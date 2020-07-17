# Feature Extraction & Embeddings

## Bag of Words

You can treat a collection of documents as a bag-of-words for comparison purposes. For instance, if you want to check the plagirism of student's essays, then you can treat each essay as bag of words. In order to obtain BOW, we need to follow appropriate pre-processing (normalization, cleaning, lemmatization etc) steps.<br>

<img src="./images/1. BOW.png" height="200"></img><br><br>

 But after pre-processing, keeping them as separate sets is very inefficient.<br>
 
 <img src="./images/2. text cleaning.png" height="160"></img><br><br>
 
 
A better approach is to treat each word document into vector of numbers. A set of documents is known as *Corpus*. First step is to collect all unique words from your corpus to form a *Vocabulary*.<br><br>

 <img src="./images/4. Corpus & Vocab.png" height="200"></img><br><br>


Second, we need to create a *document-text table* where we fill in the frequency of each word occuring in the document. <br><br>

<img src="./images/3. matrix.png" height="200"></img><br><br>

## TF-IDF

One disadvantage of BOW is that it treats every word equally even though we know that there are some words which are of greater importance/weightage. To overcome this we introduce TF-IDF resemblency, where in the document-matrix, we also take note of in how many documents did that word appear and divide the frequency of words by the number of documents in which that word has appeared. <br>

<img src="./images/6. TF-IDF Matrix.png" height="200"></img><br><br>


*This gives us a metrics which is directly propotional to term frequency (TF) but is inversely propotional to document frequency (IDF). Hence the term TF-IDF.*

<img src="./images/5. TF-IDF.png" height="200"></img><br><br>



## One-Hot Encoding

One-hot encoding is similar to BOW except here, we treat each word like a class and assign it a vector that has 1 in a single pre-determined position for that word and 0 for the rest.<br><br>

<img src="./images/7. One-Hot Encoding.png" height="200"></img><br><br>







