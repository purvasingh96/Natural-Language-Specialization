# Week 1 : Logistic Regression

## NLP Libraries

1. Importing twitter dataset from NLTK :

```python
import nltk                                # Python library for NLP
from nltk.corpus import twitter_samples    # sample Twitter dataset from NLTK
```

2. For NLP, the preprocessing steps are comprised of the following tasks:<br>
a. Tokenizing the string<br>
b. Lowercasing<br>
c. Removing stop words and punctuation<br>
d. Stemming<br>

```python
# download the stopwords from NLTK
nltk.download('stopwords')

import re                                  # library for regular expression operations
import string                              # for string operations

from nltk.corpus import stopwords          # module for stop words that come with NLTK
from nltk.stem import PorterStemmer        # module for stemming
from nltk.tokenize import TweetTokenizer   # module for tokenizing strings

# instantiate tokenizer class
tokenizer = TweetTokenizer(preserve_case=False, strip_handles=True,
                               reduce_len=True)

# tokenize tweets
tweet_tokens = tokenizer.tokenize(tweet2)

```

3. Stemming
Stemming is the process of converting a word to its most general form, or stem. This helps in reducing the size of our vocabulary.

```python
# Instantiate stemming class
stemmer = PorterStemmer() 
stemmed_word = stemmer.stem(word)
```


