## Computational Experiments

A lot of experiments in my research areas involve working with simulations of algorithms operating on synthetic or real data. This means that there are often many different ways of understanding how to set up an appropriate experimental validation of your theoretical or algorithmic ideas. What follows is one approach to figuring out how to set up and run your experiments. In this, I assume you have the algorithm working properly (i.e. the bugs have been worked out).

The central thing to figure out is the set of questions your want your experiments to answer. These questions have to be specific and answerable in a single plot/table/diagram/etc. It is tempting to run a bunch of simulations first and then figure out what questions to ask later but you will invariably end up asking different questions than you should or having to rerun of new simulations. 

So what do I mean by specific and answerable? Let's do an example of refining a too-general question into something more workable. Suppose you have an algorithm for training a predictor on labeled data (a supervised learning algorithm). The algorithm has parameters A and B. Starting from the top:

* How good is my algorithm?
* How does the test error of my algorithm behave?
* What is the test error of my algorithm as a function of the sample size?
* How does the test error decrease with the number of training points?
* How does the test error decrease with the number of training points for small A?
* How does changing B affect how my test error decreases with the number of training points when A is small?

At the end you can answer this question with a plot that has several plots (one for each value of B) of error versus training set size for fixed A.

When figuring out what to do for experiments you want to write down the list of performance criteria (e.g. test error, run time, memory usage, bandwidth) and a list of algorithm parameters (A, B, sample size, bound on the norm of input points, etc.). You will be fixing some of these and seeing how the others behave. Or you will be constraining one of the performance criteria (e.g. make sure the memory doesn't exceed 1 Gb).

When preparing to do experiments:

* Make a list of questions first. **Write them down.**
* Figure out what simulations to run.
* Determine how to visualize your results.
* Interpret your results (e.g. answer the question).

As with your research notes (see above), a slide deck that grows over time where you can document each day, findings, etc. in your experiments can be really helpful. As before, make sure you have lots of text in there too so that you know what you are thinking and what worked and didn't work and what makes sense and doesn't make sense. You don't have to share these slides with anyone. They are for you alone so you can treat it almost like a diary.
