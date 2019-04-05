# RNNs with Pytorch and Crayons

Assuming you all know what a basic multilayer neural network is.

So in a normal neural network (NNN!), the hidden state of the n'th layer is a function of the output of the (n-1)th layer. In an RNN we make this only a little more complicated- the n'th layer is a function of the (n-1)th layer and the previous hidden state of the current layer.

Hence, not only does an RNN have layers, in an RNN we also get the notion of **timesteps**.

## A Few Initial Formalities

The inputs and the sizes of the data required.

```python
import torch.nn as nn
INPUT_SIZE = 2
HIDDEN_SIZE = 2
```

## f(x, ht)

The block representations honestly don't help me much, so here's the pure function:

## Types of RNN Cells

Each "cell" of an RNN is a function that takes, not one, but *two* inputs: the direct input to the function, and the previous hidden state of the cell itself.

### GRU as an RNN

Using this theory, we can see that LSTMs and GRUs are also RNNs, with very complicated functions. The GRU function is usually visualized as three "gates", but you can put it into one single function and it just starts looking like a very complicated NN with six weight vectors. Which it is- albeit an NN which employs a recursive function.

Practically, this is a GRU cell:

<pic of equation>

Fortunately for all non-mathematicians, pytorch helpfully abstracts out this gigantic equation into a class `GRUCell`.

```python
gru = nn.GRUCell(INPUT_SIZE, HIDDEN_SIZE)
```

### LSTM as an RNN

An LSTM has an even more fun equation:

<pic of equation>

And once again, pytorch abstracts this into LSTMCell:

```python
lstm = nn.LSTMCell(INPUT_SIZE, HIDDEN_SIZE)
```




