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

## Head component

The head component in the Transformer architecture is a single self-attention layer that performs attention on a given input sequence. The self-attention mechanism allows the model to weigh the importance of different positions in the input sequence, enabling it to capture long-range dependencies and relationships between tokens.

The head component has three learnable linear transformations: key, query, and value. These transformations project the input sequence into a lower-dimensional space, called the embedding space. The dimensions of the embedding space are usually smaller than the input sequence dimensions, making the computations more efficient.

The key and value projections are applied to the input sequence to obtain the key and value matrices, respectively. The query projection is applied to the same input sequence to obtain the query matrix. The attention weights are then computed by taking the dot product of the query and key matrices and scaling it by a scaling factor.

The attention weights are then passed through a softmax activation function to obtain the final attention weights. These weights are then used to weight the value matrix, producing the output of the self-attention layer.

In multi-head attention, multiple head components are used in parallel, each with different learnable parameters. The outputs of the different heads are concatenated and passed through another linear transformation to obtain the final output of the multi-head attention layer.

