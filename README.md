# PyTorch-Practice
Just Playing around with Pytorch


## Learning Transformers
Learning about Transformers from scratch.

First we can start with understanding of self attention 
then we can look at some models for eg bert etc

## Intuition Behind Self attention :
The fundamental operation of any transformer architecture is the self-attention operation.
 Say we’re calculating the self-attention for the first word in this example, “Thinking”. We need to score each word of the input sentence against this word. The score determines how much focus to place on other parts of the input sentence as we encode a word at a certain position.

### Why do we need self attention?
Ans: Suppose we have input  *this restaurant was not terrible*  here using other methods (independent methods BOW) this may get classified as negative review because of the word terrible. But to say this was a postive review we need the model to understand that the meaning of the word *terrible* is actually inverted by *not*. So if we do self attention on these embedding vectors, self attention may learn to undertand the actual sentiement of this statement. 
The score is calculated by taking the dot product of the query vector with the key vector of the respective word we’re scoring

Now we add cool things to self attentions when using in transformer :
1. **Scaled dot Product**
2. **Keys, values and query transformation**
3. **Multi head tranformation**

### 1. Scaled dot product 
Since dimensionality of input vector can grow, making the dot product large or very small, which can cause problem in training, therefore we divide it with √K to normalize it.

### 2.Keys, values and query transformation
- We can treat Attention as a soft dictionary
- Where every key matches the query to some extent, as determined by there dot product
- a mixture of all values is returned with softmax-normlaized dot products as mixture weights

### 3.Multi head tranformation
It expands the model’s ability to focus on different positions. Yes, in the example above, z1 contains a little bit of every other encoding, but it could be dominated by the the actual word itself.
It gives the attention layer multiple “representation subspaces”
### Resources I used to understand Transformer

1. https://jalammar.github.io/illustrated-transformer/
2. http://peterbloem.nl/blog/transformers
3. https://github.com/huggingface/transformers/blob/v4.16.2/src/transformers/models/bert/modeling_bert.py
