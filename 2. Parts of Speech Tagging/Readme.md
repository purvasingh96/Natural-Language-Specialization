# Parts of Speech Tagging

## Overview

In corpus linguistics, part-of-speech tagging (POS tagging or PoS tagging or POST), also called grammatical tagging is the process of marking up a word in a text (corpus) as corresponding to a particular part of speech, based on both its definition and its context.

<img src="./images/1. pos tagging.png" height="150"></img>

## Lookup Table

In look-up table we try to create a matrix, where each word is tagged. Using look-up table we try to tag parts of speech of a new sentence. For example - <br>
<img src="./images/2. look-up table.png" height="240"></img><br>

Considering the above example, the problem with look-up tables is that it is tagging *Will* also as a *Modal* and not a *Noun*. This problem can be solved using *Bigrams*

## Bigrams

In Bigrams, we not just look at words, we look at their neighbours as well and we tag *pairs of words* instead. <br>
<img src="./images/3. Bigrams.png" height="240"></img>
