## [All papers](../papers.md)
## [Attention is all you need, Transformer paper](https://arxiv.org/pdf/1706.03762.pdf)
[Here](http://jalammar.github.io/illustrated-transformer/) is The Illustrated Transformer, and [here](http://nlp.seas.harvard.edu/2018/04/03/attention.html) is The Annotated Transformer(Pytorch)
1. abstract:
    1. Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely.
    2. parallelizable and requiring significantly less time to train.
    3. WMT 2014 English-to-German translation: 28.4 BLEU(2 over the existing best results)
    4. WMT 2014 English-to-French translation: 41.8 BLEU, 3.5 days on eight GPUs.
    5. generalize well by appling on English constituency parsing both with large and limited training data. 
2. introduction
3. architecture 
    1. Encoder: composed of a stack of N=6 identical layers.  Each layer has two sub-layers. The first is a multi-head self-attention mechanism, and the second is a simple, position-wise fully connected feed-forward network. 
    2. Decoder: also composed of a stack of N= 6 identical layers. In addition to the two sub-layers in each encoder layer, the decoder inserts a third sub-layer, which performs multi-headattention over the output of the encoder stack.
    3. Each word is embedded into a vector of size 512. 
4. conclusion
