## [All papers](../papers.md)
## [Luong Attention, Effective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/pdf/1508.04025.pdf), or another [pdf](https://nlp.stanford.edu/pubs/emnlp15_attn.pdf)
1. abstract:
    1. **global** attention: all source words are attended, **local** attention: a subset of source words are considered 
    2. WMT15 translation task, English and German in both directions. ensemble model using different attention architectures
2. introduction
    1. NMT is appealing since it requires minimal domain knowledge and is conceptually simple.
    2. examined  various  alignment functions for attention-based models.
3. architecture 
    1. encoder: BiRNN
    2.  The context vectorc  is then derived as a weighted average over the set of source hidden states within the window.
        1. Monotonic alignment(local-m) 
        2. Predictive alignment(loca-p)
    3. Input-feeding Approach: in  standard  MT, a coverage set  is  often  maintained  during  the translation process to keep track of which source words  have  been  translated. Likewise, in attentional NMTs, attentional  vectors are concatenated with inputs at the next time steps.
4. train
    1. datasets: WMT14 English German in both directions, using 50K words for both language.
    2. **Matlab code**, single GPU, **7-10** days to complete training.
    3. training details given, many parameters included.
