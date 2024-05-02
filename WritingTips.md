## Writing tips

Writing is hard!

One of the best books I read on writing was Harold Becker's *Writing for Social Scientists* (in the lab Google Drive or you can find it online). It says "for social scientists" but has a lot of general advice which can help when you are writing.

One of the main takeaways is that writing is 99% rewriting. Be prepared for writing to take lots of time: more time than you think it should.

As always, Raul Pacheco has some [great tips](http://www.raulpacheco.org/2013/02/improving-your-academic-writing-my-top-10-tips/).

### Getting started

When you sit down to formally write up your results into something that looks like a paper, it's time to get a bit more organized and systematic. You might be incorporating work from a [previous writeup](MakingWriteups.md), handwritten notes, and/or just little snippets and fragments from an email thread. Regardless of what you have so far, *make a fresh document*. 

One of the hardest things about writing is getting started. Staring at a blank page can be quite intimidating. But there are a couple of ways to get started. 

* Mind maps: a mind map is a graph where you can write down little ideas/concepts and link them to help you organize your thoughts. There are lots of explanations online.
* Outlining: making a detailed outline of your paper/writeup is a good starting place. You can go all the way down to outlining paragraph-by-paragraph if necessary. What an outline can do is break the writing task into more manageable pieces. Depending on what you are writing, there are outlines to start with, such as:
  * Introduction
  * Model/Problem Statement
  * Proposed Algorithm
  * Analysis
  * Experiments
  * Discussion/Conclusion
* If you are writing up a proof or some analysis, you can also outline just that part so you can break down the steps of the argument that you need to make, like
  * Decomposing the error
  * Bounding $\beta_1$
  * Bounding $\beta_2$
  * Formulating the error as a recursion
  * Putting all the pieces together
* Avoiding censoring: sometimes when writing it is best to start by just putting any text on the page and then later going back to edit it. Becker has some advice on this as well. This works especially if you have a lot of ideas but are not sure how to organize them. Writing down all your thoughts (even if in half sentences and non-grammatical) puts it all down on paper and lets you go back and organize it.
* Being verbose: start out by writing lots of explanation of what you are doing and why. For example: "Now what we need to do is upper bound $\beta^2(x)$ by a constant that does not depend on $x$. There are two ways to do this: one by analyzing the recursion in equation (5) and the other by doing a Taylor series expansion. Let's try the second approach first." That way when you go back to those notes later you will remember what you were thinking at the time. 

Always, always, always keep in mind who your *intended reader* is. This will change the way you write things! You may be writing for yourself, writing for a student in a class, writing for a peer/colleague, writing for an expert in your sub-problem, or writing for someone else entirely. Here I'm using ``writing'' but it can also mean giving a talk, teaching a class, etc.


### Technical writing

I learned many of the rules of mathematical writing from this handout from when I was an undergradute:

* [Writing a Math Phase Two Paper](http://web.mit.edu/18.704/www/piiUJM2.pdf). There is an HTML [(older version)](http://web.mit.edu/mathp2/www/piil.html)

Mathematical writing is its own skill and it not the same writing that you would do on a homework or exam. This is often the hardest thing for graduate students to learn. It takes *practice*.

If you plan to submit to a conference, **use the template** from the conference website. Templates change over time, sometimes in small ways, and the last thing you want is to have the server reject your PDF for some formatting violation caused by you using the previous year's template (this has happened to me). Using the template also prevents some of the weird LaTeX compilation errors.

Finally, remember that when you sit down to write, you're going to be doing a lot of editing and rewriting afterwards. Resist the urge to try and apply constraints or formatting hacks: save it for the editing stage. "Making it fit into the page limits" is something you can work on *after* your ideas are cleanly and clearly written. Don't put any \vspace{-0.5cm} or stuff like that: focus on the *content*.

Focus on getting the ideas you want to say in an order that would make sense to someone who doesn't know the problem you're working on. For example, imagine a classmate of yours from undergrad or grad school. I find outlining helps a lot, and then refining the outline with more and more details until you have manageable chunks that you can actually write.

#### Introduction

Write the introduction after the main body of the paper is written. The introduction is where you tell the story of the paper and until you have the technical details more solidified, it's impossible to tell the story accurately. There are several parts of an introduction for a paper:

* **Motivating the problem.**
* **Explaining the approach.**
* **Related work.**
* **Explaining your contribution.**

**To be finished later**

#### Problem statement/model

The second section of a paper is usually the model or problem statement. Here is where you set up the notation you are going to use for the rest of the paper. It's important to set all of this up precisely and consistently, or else you are going to waste a lot of time with inconsistent notation and equations that don't make sense.

* **Notation.** This is where you set up *generic* notation conventions and notation which will be used throughout the paper. For example, you might say "For a positive integer $n$, let $[n] = \{1,2,\ldots, n\}$." Or you might say "We use boldface for random variables and roman type for realizations." Do not mix up generic notation conventions (boldface means this, calligraphic means that) and specific notation useed in setting up the problem you are studying. These are conceptually different things!

* **The model/problem.** This is where...

**To be finished later**


#### Grammar and structure

Here are some writing in English tips which I have had injected (metaphoricallly) into me from $N \gg 1$ of classes. Note that as an American, I basically only know one language, and it's questionable whether I even know it that well. American English is only one type of English! So these are not prescriptive (you have to do it this way) but more notes on what does and doesn't read as well to an American reader.

* Many writers think that long, complicated sentences are more sophisticated. In reality, they are harder to read. You can introduce more complex sentence structure later. For the early drafts, just stick to short and simple sentences.
* Passive voice. You will read a lot of technical writing that is written in passive voice. For example: "it was shown by Wang and Xie that A = B [1]." Passive voice is not always bad! But it's more direct and clear (often) to write an actice sentence: "Wang and Xie showed that A = B [1]."  
* It is tempting to add capitalization to things but is often not needed.  
BAD: "the algorithm is $\epsilon$-Differentially Private", "we will use  Complex Analysis to solve this problem."   
GOOD: "the algorithm is $\epsilon$-differentially private", "we will use complex analysis to solve this problem."

#### Over and under-explaining

When using various mathematical results in your proof, you have to strike a balance between over- and under-explaining and between basic facts and research results. You can of course try to prove everything back to the very foundations of mathematics but that's a waste of space.

Let's take an example: you want to use the triangle inequality for the $\ell_p$ norm to show $\|a + b\|_p \le \|a\|_p + \|b\|_p$. Here are some options:

* Use it without comment/explanation. This is maybe OK if you think that it's obvious to your *intended reader* that the $\ell_p$ norm is a norm.
            
* Write "by the triangle inequality..." This is short and clear and implies that the reader should know why the triangle inequality holds.
            
* Write "by Minkowski's inequality..." and cite his original book. This is technically correct (Minkowski proved that the $\ell_p$ norm is a norm). However, this is really a "textbook" result. In a sense it's *less* clear to put his name on it and cite this German book which you probably didn't read. If you want to use a textbook result, cite a book you have read and have access to.
            
* Cite a modern textbook. Just check if they call it "Minkowski's inequality" or if they give it as a result and mention in the text that it was proved by Minkowski. This is important because the exact statement that you use in your proof may not be the same as how Minkowski stated it. You always want to use the closest form of the result to what you need.
            
In this particular case, it might be less clear to call the triangle inequality Minkowski's Inequality because some (many?) readers might not remember that Minkowski proved it, but they do remember that $\|\cdot\|_p$ is a norm.

#### Punctuation and so on

* Watch out for extra commas! That is, don't write "Watch out, for extra commas!" or "Watch out, for, extra commas!" We (myself included) tend to put in extra commas as pauses in thought, but then it actually looks a bit odd when reading.
* Don't use citations as nouns. This is a *hard thing to avoid*. But in some publications citations turn into footnotes so if you write "In<sup>1</sup> it is shown that..." it will look bad. Of course, for IEEE formats you have square brackets so "In [3] it was shown that..." looks fine. But don't do it! 
* Everyone likes to see their name in print, so consider occasionally using "Vershynin [3] shows that" is nice.
    
#### Minor pet peeves

* If using "use" works where you wanted to write "utilize", then use "use" instead.
* "upto" should be "up to"


### Editing

Once you get the ideas in the right order, the technical material written, and the major issues out of the way, it may come time to "polish" the manuscript. What I call "polishing" is an iterative process to edit and improve the manuscript. 

There is a ton of advice out there on editing and writing. Here are a few references which I think are extremely helpful:

* [Common errors](https://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)
* Howard S. Becker, Writing for Social Scientists, University of Chicago Press, 2007.  
You may think that this is not a book engineers need to read but it has lots of great advice about the writing process, especially in the first few chapters.


