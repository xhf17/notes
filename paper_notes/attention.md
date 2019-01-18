## [All papers](../papers.md)
## [Neural Machine Translation By Jointly Learning to Align and Translation, Original sequence-to-sequence + attention paper](https://arxiv.org/pdf/1409.0473.pdf)
1. abstract:
    1. translation, encoder, decoder, fixed-length
    2. conjecture: a fixed-length vector is a bottleneck.
    3. propose attention: search for parts of a source sentence that are relevant to predicting a target word
    4. achieve a translation performance comparable to the existing state-of-the-art **phrase-based** system on the task of English-to-French translation.  Furthermore,
    5. find alignments.
2. introduction
    1. A potential issue with this **encoder–decoder** approach is that a neural network needs to be able to **compress** all the necessary information of a source sentence into a fixed-length vector. Difficult for long sentence, performance deteriorates rapidly as length.
    2. attention:  positions most relevant information is concentrated. predict based on the context vectors associated with these source positions and all the previous generated target words
    3. distinguishing feature: does not encode or squash a input into a fixed-length vector. Instead, it encodes the input into a sequence of vectors and chooses a subset of these vectors adaptively while decoding.
3. architecture 
    1. encoder: BiRNN
    2. attention calculation: refer to origin paper.
4. conclusion
    1. datasets: WMT14 English-to-French, using 30K words for both language.
    2. train 2 modles, twice for 30-length and 50-length: proposed and RNN Encoder–Decoder models, time cost: 5 days.
