## Computational Experiments

A lot of experiments in my research areas involve working with simulations of algorithms operating on synthetic or real data. This means that there are often many different ways of understanding how to set up an appropriate experimental validation of your theoretical or algorithmic ideas. What follows is one approach to figuring out how to set up and run your experiments. In this, I assume you have the algorithm working properly (i.e. the bugs have been worked out).

The central thing to figure out is the set of questions your want your experiments to answer. These questions have to be specific and answerable in a single plot/table/diagram/etc. It is tempting to run a bunch of simulations first and then figure out what questions to ask later but you will invariably end up asking different questions than you should or having to rerun of new simulations.

So what do I mean by specific and answerable? Let's do an example of refining a too-general question into something more workable. Suppose you have an algorithm for training a predictor on labeled data (a supervised learning algorithm). The algorithm has parameters A and B. Starting from the top:

* **How good is my algorithm?** This is too big picture to be answerable with a single experiment.
* **Is the test error of my algorithm lower than previous methods?** This is getting there but not specific enough: no discussion of the parameters A and B or enough details about what is being fixed and what is being varied.
* **For what sample sizes is my algorithm's test error better than previous methods?** This fixes an x-axis (sample size) and y-axis (test error) but doesn't give you enough to really set up the experiment.
* **How fast does my algorithm's test error decrease with sample size for different choices of A and B?** This now fixes a set of experiments and implicitly you can compare to previous methods on the same plot.

You might also consider a better approach to exploring the choices of A and B. When you have many parameters the number of settings blows up rapidly (e.g. 10 training set sizes, 10 learning rate/step sizes, 20 choices of number of iterations, 50 runs per algorithm = 100000 simulations). At the end you might answer your question plot that has several subplots (one for each value of B) of error versus training set size for fixed A.

When figuring out what to do for experiments you want to write down the list of performance criteria (e.g. test error, run time, memory usage, bandwidth) and a list of algorithm parameters (A, B, sample size, bound on the norm of input points, etc.). You will be fixing some of these and seeing how the others behave. Or you will be constraining one of the performance criteria (e.g. make sure the memory doesn't exceed 1 Gb).

When preparing to do experiments:

* Make a list of questions first. **Write them down.**
* Figure out what simulations to run.
* Determine how to visualize your results.
* Interpret your results (e.g. answer the question).

As with your research notes (see above), a slide deck that grows over time where you can document each day, findings, etc. in your experiments can be really helpful. As before, make sure you have lots of text in there too so that you know what you are thinking and what worked and didn't work and what makes sense and doesn't make sense. You don't have to share these slides with anyone. They are for you alone so you can treat it almost like a diary.

When writing your experiments section in a paper or poster, it can "write itself" in the form:

* *For a paper:* **Our question.** In order to understand this we **ran this experiment**. The results are shown in Figure 5, which plots **the visualization we used for the result**. As we can see **this answers our question in the following way**.
* *For a poster:* You can write the question, show the plot, and give the conclusion all together and when presenting the poster describe the experiment in more detail (or put the details on the poster if it's simple). Use descriptive legends and header text!
