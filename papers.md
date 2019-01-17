# Notes for papers
* [NLP](#NLP)
  * [embedding](#embedding)
  * [seq2seq](#seq2seq)
* [ML](#ML)
* [paper notes](#paper-notes)
## NLP
### embedding
* [GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/pubs/glove.pdf)
* [Word2Vec Tutorial - The Skip-Gram Model](http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/)
### seq2seq
* [Sequence to Sequence Learning with Neural Networks](https://arxiv.org/pdf/1409.3215.pdf)
  #### notes:
* [Neural Machine Translation By Jointly Learning to Align and Translation, Original sequence-to-sequence + attention paper](https://arxiv.org/pdf/1409.0473.pdf)
* [Attention is all you need, Transformer paper](https://arxiv.org/pdf/1706.03762.pdf)
  #### notes
  1. abstract:
      1. Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely.
      2. parallelizable and requiring significantly less time to train.
      3. WMT 2014 English-to-German translation: 28.4 BLEU(2 over the existing best results)
      4. WMT 2014 English-to-French translation: 41.8 BLEU, 3.5 days on eight GPUs.
      5. generalize well by appling on English constituency parsing both with large and limited training data. 
  2. introduction
  3. architecture
  4. conclusion
* [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/pdf/1810.04805.pdf)
* [A structured self-attentive sentence embedding](https://arxiv.org/pdf/1703.03130.pdf)
* [Effective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/pdf/1508.04025.pdf)
* [A Neural Conversational Model](https://arxiv.org/pdf/1506.05869.pdf)
  #### notes
  * two conversation datasets: 
    *  closed-domain: IT Helpdesk Troubleshooting dataset, using 20K words
    *  open-domain:  OpenSubtitles dataset, using a vocabulary of 100K words
  * *perplexity* with n-gram model, compared with rule-based [cleverbot](www.cleverbot.com)  using human evaluations on a set of [200 questions](http://ai.stanford.edu/~quocle/QAresults.pdf).
  * It remains an open research problem  of  designing  a  good  metric  to  quickly  measure  the quality of a conversational model
  * drawback: 
    * it only gives simple, short, sometimes unsatisfying answers to our questions.
    * another problematic drawback is that the model does not capture a consistent personality. Indeed, if we ask not identical but semantically similar questions, the answers can sometimes be inconsistent.  This is expected due to the simplicity of model and the dataset in experiments.
      > *Human*: what is your job ?
      > *Machine*: i’m a lawyer.
      > *Human*: what do you do ?
      > *Machine*: i’m a doctor.
## ML
* [PAMI papers](https://www.computer.org/csdl/trans/tp/index.html)
## paper notes
