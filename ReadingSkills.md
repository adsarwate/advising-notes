## Reading papers and literature search

### How to read a paper

There is already lots of advice on how to read papers out there. I think the first thing to decide is what kind of reading are you going to do? That is, you have to figure out what you want to learn from the paper.

* What is this area of research about?  Then you can read the introduction, conclusion, and skim the rest perhaps.
* How do they formulate their problem mathematically? You should read the intro (maybe skim some of it/read it later) and definitely read the model, problem statement, or whatever that section is called.
* What does this paper show? Read all of the above as well as the main results (but not the proofs). Focus on trying to understand what the results mean.
* How do they prove their results? In this case you want to focus on the proofs at least at the proof sketch level or even better, line by line. Try to make sure you can understand each step, or ask for help!

Always read with an objective in mind:

* *I want to learn something new.* Read and take a few notes so you remember!
* *I want to come up with a better formulation of my problem.* Try and translate that paper's notation into your own notation.
* *I need a tool to help my proof.* Copy out the lemma or theorem. Where can it apply in your problem? Does your problem satisfy all the conditions?
* *I want to see what experiments to run.* Find out where to get the data sets. Does the paper have a code repo? Are there already preprocessing scripts out there?
* *I need to find more references on this topic.* Look at the related work. Maybe you are doing a literature search (see below).

### How to do a literature search

Doing a literature search means finding all of the relevant papers on a single topic. The goal is to broad and comprehensive -- you want to find more papers/books/etc. that might be useful before you decide which ones to include in your search.

One way to start is to pick a paper that you know is on the topic and read the intro/related work section. There will be sentences like "Patel et al. [13] showed that the general problem of optimizing the rate is NP-hard, but later work by Xu and Zhang [14] gave a characterization of problems which can be efficiently optimized by solving a linear program." Then you know that the papers by Patel et al. [13] and Xu and Zhang [14] aer both relevant to the theoretical aspects of the problem. You can download those to papers and late read their related work, etc.

Another good option is to see what papers cite the paper you found by looking in Google Scholar for example. Then you can find later papers which cite the paper you are looking at. Some will seem relevant and some will be irrelevant. Download the relevant ones and do the same search procedure on them by reading the related work.

How do you decide whether to include a paper in your search? You want to search broadly but you need to categorize the papers so that you can start organizing the citations by what the papers talk about. You might have one category of primarily experimental papers, one category for theoretical analyses, one category for applications to diffent problems, and so on. Or you might have papers which are written by statisticians versus those written by electrical engineers which don't seem to cite each other but are looking at similar problems.

Some questions to help you organize your thinking around a paper you are looking at are given below. These are not exhaustive but should give you a sense of the kind of questions you should be asking before and as you read.

* Where was this published? Is this a top-tier journal or conference? Is it one you have heard of? It's easy to find papers which are published in less impactful venues which might seem to be relevant but which are actually not.
* Who are the authors and what institution (academic or industry) are they from? What kind of department are they in? This can tell you a lot about the methodology and terminology you are likely to encounter in the paper.
* What sort of paper is this: one which proposes a new model and proves new theorems, one which solves a longstanding open problem, one which proposes algorithms an analyses them, one which proposes algorithms and shows that they work experimentally, one which summarizes the work in an area, or some mix of the above?
* What kind of analytical tools do they use?
* What is the scale of the experiments: testing it out on commonly used datasets like MNIST and CIFAR-10, or application-specific data sets which are publicly available, or data which is only available to the authors?

It is quite possible to have 100+ papers that you download. That is research! You have to SEARCH and REad to understand what has been done before.


### How to write a literature review

Once you have your pile of papers and notes on the papers, you have to organize them into a coherent description of the related work on a problem.

Finally, take notes on each of the papers, and add the references to a BibTeX file so you can write up a summary. Start by writing little chunks of summary tying things togeher. For example: 

> *"the problem was first studied by Johnson [1] and sparked new work in both the physics and engineeing communities. Physicists [2-4] used statistical mechanics to understand the phenomena in very large systems. The recent survey paper by Gentile et al. [5] describes this body of research in great detail. On the engineering side, separate work by Horn and Kay [6] and Sastry et al. [7] showed that for smaller systems one could observe coupling between individual components..."* 

Then you might have a separate section which addresses experimental or algorithmics work. And so on.

Eventually you have enough fragments to try and organize them into a story. Think of how you would explain the problem to your friend and all the work that has been done. You can't do it by talking about random papers, but instead talk about different dimensions of the problem and what work has been done in those directions.

If this literature review is part of a related work section for a  paper you are wriing, then you need to describe what the paper does, what it doesn't do, and what your paper does differently. You should never (if you can avoid it) write a sentence like 

> *Patel et al. studied a similar problem [1]*. 

In what way is it similar? That sentence is almost meaningless.

