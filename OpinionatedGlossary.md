## An Opinionated Glossary

In which the author opines on technical jargon with an eye towards teaching.

### I

**Inductive Bias**: a term you hear thrown around a lot in ML papers/discussions is "inductive bias." This sounds scary and technical at first (or maybe just confusing) but if we replace the two words with some synonyms it might be clearer. 

* "Inductive" refers to an algorithm which is trying to  estimate something or fit a prediction model, etc. For example, stochastic gradient descent (SGD) is trying to induce, from the training data, a setting of the parameters (weights in a DNN). People use this word because of the philosopher Hume's famous [problem of induction](https://en.wikipedia.org/wiki/Problem_of_induction) (I think).
* "Bias" here means preference, not statistical bias like $\mathbb{E}[\hat{\theta}] = \theta$.

So "what is the inductive bias" means "what kinds of models does the algorithm prefer? By insisting on "distribution free" assumptions and thinking that they are just "learning from the data" they push the agency/bias away from the person doing the inference (e.g. a data analyst) onto the algorithm. But the algorithm can't have bias in the "preference" sense of the word, so this to me feels a bit like shifting the blame of bias from the implicit modeling assumptions (made by people) onto something which can't be held morally accountable for actual bias, just technically accountable.

See also [Cosma Shalizi's notebook](http://bactra.org/notebooks/learning-inference-induction.html).


