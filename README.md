# PyTorch-Practice
Just Playing around with Pytorch


## Learning Transformers
Learning about Transformers from scratch.

First we can start with understanding of self attention 
then we can look at some models for eg bert etc


### Why do we need self attention?
Ans: Suppose we have input  *this restaurant was not terrible*  here using other methods (independent methods BOW) this may get classified as negative review because of the word terrible. But to say this was a postive review we need the model to understand that the meaning of the word *terrible* is actually inverted by *not*. So if we do self attention on these embedding vectors, self attention may learn to undertand the actuall sentiement of this statement.

Now we add cool things to self attentions when using in transformer :
1. **Scaled dot Product**
2. **Keys, values and query transformation**
3. **Multi head tranformation**

### 1. Scaled dot product 



### Resources I used to understand Transformer

1. https://jalammar.github.io/illustrated-transformer/
2. http://peterbloem.nl/blog/transformers   