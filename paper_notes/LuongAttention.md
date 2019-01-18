## [All papers](../papers.md)
## [Effective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/pdf/1508.04025.pdf)
1. abstract:
    1. translation, encoder, decoder, fixed-length
2. introduction
    1. A potential issue with this **encoder–decoder** approach is that a neural network needs to be able to **compress** all the necessary information of a source sentence into a fixed-length vector. Difficult for long sentence, performance deteriorates rapidly as length.
3. architecture 
    1. encoder: BiRNN
4. conclusion
    1. datasets: WMT14 English-to-French, using 30K words for both language.
