# RNN

## What are RNN’s?
The idea behind RNNs is to make use of sequential information. In a traditional neural network we assume that all inputs (and outputs) are independent of each other. But for many tasks that’s a very bad idea. If you want to predict the next word in a sentence you better know which words came before it. RNNs are called recurrent because they perform the same task for every element of a sequence, with the output being depended on the previous computations and you already know that they have a “memory” which captures information about what has been calculated so far.

```
rnn = RNN()
y = rnn.step(x) # x is an input vector, y is the RNN’s output vector
```

## Different types of RNN’s
The core reason that recurrent nets are more exciting is that they allow us to operate over sequences of vectors: Sequences in the input, the output, or in the most general case both. 

### One-to-one:
This also called as Plain/Vaniall Neural networks. It deals with Fixed size of input to Fixed size of Output where they are independent of previous information/output.
* Ex: Image classification.

### One-to-Many:
it deals with fixed size of information as input that gives sequence of data as output.
* Ex: Image Captioning takes image as input and outputs a sentence of words.

### Many-to-One:
It takes Sequence of information as input and ouputs a fixed size of output.
* Ex: sentiment analysis where a given sentence is classified as expressing positive or negative sentiment.

### Many-to-Many:
It takes a Sequence of information as input and process it recurrently outputs a Sequence of data.
* Ex: Machine Translation, where an RNN reads a sentence in English and then outputs a sentence in French.

### Bidirectional Many-to-Many:
Synced sequence input and output. Notice that in every case are no pre-specified constraints on the lengths sequences because the recurrent transformation (green) is fixed and can be applied as many times as we like.
* Ex: video classification where we wish to label each frame of the video.
