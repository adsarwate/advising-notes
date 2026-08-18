## Computational Experiments

A lot of experiments in my research areas involve working with simulations of algorithms operating on synthetic or real data. This means that there are often many different ways of understanding how to set up an appropriate experimental validation of your theoretical or algorithmic ideas. What follows is one approach to figuring out how to set up and run your experiments. In this, I assume you have the algorithm working properly (i.e. the bugs have been worked out).

### Designing/asking questions

The central thing to figure out is the set of questions your want your experiments to answer. These questions have to be specific and answerable in a single plot/table/diagram/etc. It is tempting to run a bunch of simulations first and then figure out what questions to ask later but you will invariably end up asking different questions than you should or having to rerun of new simulations.

So what do I mean by specific and answerable? Let's do an example of refining a too-general question into something more workable. Suppose you have an algorithm for training a predictor on labeled data (a supervised learning algorithm). The algorithm has parameters A and B. Starting from the top:

* **How good is my algorithm?** This is too big picture to be answerable with a single experiment.
* **Is the test error of my algorithm lower than previous methods?** This is getting there but not specific enough: no discussion of the parameters A and B or enough details about what is being fixed and what is being varied.
* **For what sample sizes is my algorithm's test error better than previous methods?** This fixes an x-axis (sample size) and y-axis (test error) but doesn't give you enough to really set up the experiment.
* **How fast does my algorithm's test error decrease with sample size for different choices of A and B?** This now fixes a set of experiments and implicitly you can compare to previous methods on the same plot.

You might also consider a better approach to exploring the choices of A and B. When you have many parameters the number of settings blows up rapidly (e.g. 10 training set sizes, 10 learning rate/step sizes, 20 choices of number of iterations, 50 runs per algorithm = 100000 simulations). At the end you might answer your question plot that has several subplots (one for each value of B) of error versus training set size for fixed A.

### Running the experiments

When figuring out what to do for experiments you want to write down the list of performance criteria (e.g. test error, run time, memory usage, bandwidth) and a list of algorithm parameters (A, B, sample size, bound on the norm of input points, etc.). You will be fixing some of these and seeing how the others behave. Or you will be constraining one of the performance criteria (e.g. make sure the memory doesn't exceed 1 Gb).

When preparing to do experiments:

* Make a list of questions first. **Write them down.**
* Figure out what simulations to run.
* Determine how to visualize your results.
* Interpret your results (e.g. answer the question).

As with your research notes (see above), a slide deck that grows over time where you can document each day, findings, etc. in your experiments can be really helpful. As before, make sure you have lots of text in there too so that you know what you are thinking and what worked and didn't work and what makes sense and doesn't make sense. You don't have to share these slides with anyone. They are for you alone so you can treat it almost like a diary.

### Writing up your results

When writing your experiments section in a paper or poster, it can often "write itself" if you stick to a general template.

#### For a paper

Try the following sectioning: is written for ML papers but can adapt easily to other scenarios.

##### Datasets, models, computation

What datasets did you use? What kind of data is in them, what are the "canonical" tasks for which this dataset has been used in prior work? Why did you choose these datasets? Why didn't you look at other datasets? Make sure to properly attribute the datasets with citations: making a dataset is a lot of work and people should be credited. Usually the website where you get the dataset (e.g. UC Irvine Repository, Hugging Face) will have information on how to cite the dataset.

What models/algorithms did you implement? Why implement those and not others/why is this a fair comparison? Again, be sure to cite the authors of the other methods. 

What computational resources were involved/needed? This is important because it matters whether you can run a simulation on a laptop or you need to buy API access to Claude.

##### Findings

I would put one subsection for each major finding in your paper. You can title the subsections with the "punchline", like "My Algorithm converges exponentially fast," or with the goal of the experiment, like "Comparison of convergence rates," or with the question, like "How do convergence rates compare?" Other things can work too. Just remember that the subsection title should be informative.

Within each subsection, you can follow a template (obviously change the phrasing etc but these things need to be there).
* **What was the question you wanted to answer?** You should have already had a question in mind so you can describe it it here. Also explain why this is an interesting/relevant/important question to answer. For example, "for our method to be useful in practice we need to understand how runtime scales with the input size."
* **What experiment did you run?** Be specific here and explain how many simulations you ran (e.g. averaged over 10 runs) and how parameters/hyperparameters were chosen.
* **Why does that answer the question?** Many people miss this step. Sometimes it's not obvious why the experiment you chose is the right one.
* **Where are the results shown?** Usually this is in a figure or table. Make sure the figure is readable and captioned well.
* **What is important to note about the results?** You want the reader to focus on the things that are important. You also want to note other interesting features, even if they are bad. Like maybe your method works well for large sample sizes but is terrible for small sample sizes.
* **What is the answer to the question you originally asked?** If it did answer the question, what was the answer? If it partially answered the question, what was answered and unanswered?

**Reminder for figures/tables:** in a paper or in a poster or in a talk.
* Make sure they are readable! Use thicker lines and larger text than you think you need. Use line style (solid, dashed) and color (but use a colorblind-friendly palette) to make distinctions. Don't forget the legend.
* Highlight the important things that you want people to notice. This is especially true in tables. Many papers just bold the number corresponding to the best performance but you can also use colors or shading in the backround of the cell. LaTeX packages that can help include `booktabs`, `multirow`, `makecell`, and the `color` option for `xcolor` (i.e. `\usepackage[table]{xcolor}`).
* For papers, make the captions informative (for posters also but you can put the caption in larger text on a poster). There are some reviewers who will look at the figures first before reading the paper. They should still get something out of it. So don't write ``$$\ell$$ versus $$n$$'' but instead ``empirical loss $$\ell$$ versus number of samples $$n$$''
* For a poster, you can write the question, show the plot, and give the conclusion all together in bullets on the poster. When presenting the poster, describe the experiment in more detail (or put the details on the poster if it's simple). Use descriptive legends and header text!
* For a talk, the first two bullet points are still important. If you can, do not just clip out the figure from the paper and put it in the talk. For the talk you want to choose what you want the audience to focus on and omit the rest. If you put a big table up there they will just read the table and try to puzzle it out and not listen to you.
