## [All papers](../papers.md)
## [A Neural Conversational Model](https://arxiv.org/pdf/1506.05869.pdf)
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
