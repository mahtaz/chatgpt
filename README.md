# chatgpt
This notebook contains transformer-based bigram language model that generates text which consists of several components:
* `Head` is a single head of the self-attention mechanism.
* `MultiHead Attention` uses multiple heads of self-attention in parallel.
* `FeedFoward` defines a linear layer followed by a non-linearity.
* `Block` is the Transformer block, which performs communication followed by computation.
* `BigramLanguageModel` is the language model that uses the Transformer architecture.

<p align="center">
  <img src="https://github.com/mahtaz/chatgpt/blob/main/images/transformer%20(2).jpg" alt="tranformer" height="500">
</p>

##  What is attention?
It involves answering what part of the input should I focus on. For example in the case of translation We want to answer how relevant is the word in the
sentence relevant to other words in the same sentence for every word. We can have an attention vector generated which captures contextual relationships
between words in the sentence as shown below.

<p align="center">
  <img src="https://github.com/mahtaz/chatgpt/blob/main/images/attention%20(2).jpg" alt="tranformer" height="500">
</p>
