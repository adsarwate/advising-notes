# Becoming a graduate researcher

**THIS IS BEING SPLIT INTO MULTIPLE FILES, stuff will vanish from here beware!!!**


## Research Skills

There are a lot of different concrete skills that you (should) develop as a graduate student. A lot of these have to do with successfully grappling with the vast amount of research that already exists: how to read it, how to evalute it critically, how to organize and summarize it, and how to present it.


## Writing tips

General writing advice:

* Writing is hard! It is 99% rewriting. Be prepared for writing to take lots of time: more time than you think it should.
* Read Harold Becker's Writing for Social Scientists (in the lab Google Drive or you can find it online). It says "for social scientists" but has a lot of general advice which can help when you are writing.
* [Improving your academic writing: My top 10 tips](http://www.raulpacheco.org/2013/02/improving-your-academic-writing-my-top-10-tips/)
* Get used to writing notes and other mini writeups in LaTeX. This will both help you get more proficient with LaTeX but also the act of writing down can help in trying to understand things. For example, suppose you want to use a theorem from some paper or book. Copy out the theorem and 


### Getting started with writing

One of the hardest things about writing is getting started. Staring at a blank page can be quite intimidating. But there are a couple of ways to get started (see also the advice from the Becker book).

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
* Being verbose: start out by writing lots of explanation of what you uare doing and why. For example: "Now what we need to do is upper bound $\beta^2(x)$ by a constant that does not depend on $x$. There are two ways to do this: one by analyzing the recursion in \eqref{eq:recursion} and the other by doing a Taylor series expansion. Let's try the second approach first." That way when you go back to those notes later you will remember what you were thinking at the time. 



### Editing and rewriting

There is a ton of advice out there on editing and writing. Here are a few references which I think are extremely helpful:

* [Common errors](https://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)
* Howard S. Becker, Writing for Social Scientists, University of Chicago Press, 2007.  
You may think that this is not a book engineers need to read but it has lots of great advice about the writing process, especially in the first few chapters.

For some very specific advice (big and small) regarding mathematical writing, see the tips section of [this overleaf template](https://www.overleaf.com/read/hczfttksjhqs)


#### Starting out

When you sit down to formally write up your results into something that looks like a paper, it's time to get a bit more organized and systematic. You might be starting from some other informal writeup in LaTeX, or just handwritten notes, or just little snippets and fragments from an email thread. Regardless of what you have so far, *make a fresh document*. 

I learned many of the rules of mathematical writing from this handout from when I was an undergradute:

* [Writing a Math Phase Two Paper](http://web.mit.edu/18.704/www/piiUJM2.pdf). There is an HTML [(older version)](http://web.mit.edu/mathp2/www/piil.html)

Mathematical writing is its own skill and it not the same writing that you would do on a homework or exam. This is often the hardest thing for graduate students to learn. It takes *practice*.

If you plan to submit to a conference, **use the template** from the conference website. Templates change over time, sometimes in small ways, and the last thing you want is to have the server reject your PDF for some formatting violation caused by you using the previous year's template (this has happened to me). Using the template also prevents some of the weird LaTeX compilation errors.

Finally, remember that when you sit down to write, you're going to be doing a lot of editing and rewriting afterwards. Resist the urge to try and apply constraints or formatting hacks: save it for the editing stage. "Making it fit into the page limits" is something you can work on *after* your ideas are cleanly and clearly written. Don't put any \vspace{-0.5cm} or stuff like that: focus on the *content*.

Focus on getting the ideas you want to say in an order that would make sense to someone who doesn't know the problem you're working on. For example, imagine a classmate of yours from undergrad or grad school. I find outlining helps a lot, and then refining the outline with more and more details until you have manageable chunks that you can actually write.

#### Editing

Once you get the ideas in the right order, the technical material written, and the major issues out of the way, it may come time to "polish" the manuscript. What I call "polishing" is an iterative process to edit and improve the manuscript. 

#### Final checks

When you are going to submit something it helps to go through through the manuscript several times to check one last time for the small issues. Being systematic about this will take less time and catch more bugs. You can do complete checks over the document for each of these things one by one, so a check for typos, for citations, for bibliography, for math formatting, etc. Focusing on one issue per go-through is better so that you don't miss things from context-switching.

* *Citations as nouns*: search for `\cite{}` commands and make sure you're not treating any of them as nouns. See below for more details.
* *Bibliography*: check that the bibliography looks consistent (see rules for bibliographies below) and correct.
* *Spelling and grammar*: read the paper *backwards*, sentence by sentence (or paragraph by paragraph. This helps you focus on each sentence individually to make sure it's correct.
* *Math formatting*: check that equations have autosizing delimiters and are punctuated correctly. Check that there are not extra blank lines before/after equations.


#### Making things fit

You will often end up in the situation where your paper is anywhere from a few paragraphs to several pages over the limit for wherever you are submitting. The question is how do you make it all fit?

Things **not** to do:

* Do not use `\vspace{-1mm}` or any sort of "negative" spacing. This is all manual hacking and should be avoided: let LaTeX do the layout, not you. That's the whole point of logical formatting.

The trick is to go systematically to make things fit. Work from the end of the document forward.

* Move material to the appendix or supplementary material.
* Check if you have too much "navigation" text. Conference papers are short and do not need an "organization of this paper" section. Having text at the end of sections saying what is coming next or text at the start of a section summarizing the section is nice from a reading perspective but is not always necessary. It's easy to go too far in this direction, but often this is filler.
* Edit your sentences to make them simpler. See some of the writing/editing tips and advice for this. There are a lot of "unnecessary words" that we all use when writing. For example, this document you are reading is too wordy and could uuse some editing. Read the writing guides for tips and tricks!
* Move (some) equations in-line. It's easy to go overboard on this! Any time you want to move an equation from display mode to in-line, ask yourself how important that equation is and whether it will help the reader to see it displayed/centered versus in-line.
* Manipulate figures. Shrinking figures is a way to get more space but make sure they are still legible/readable! You might want to make the lines in the plot thicker to be easier to read. Sometimes you might have an illustrative figure which helps the reader figure out what is going on: those are good targets for moving to an appendix or removing from the paper, especially if the space-to-benefit ratio is high.

### Specific common issues

There are a couple of issues which are specific to technical writing. Here are some major ones to consider.

#### Grammar and sentence structure

* Many writers think that long, complicated sentences are more sophisticated. In reality, they are harder to read. You can introduce more complex sentence structure later. For the early drafts, just stick to short and simple sentences.
* Passive voice. You will read a lot of technical writing that is written in passive voice. For example: "it was shown by Wang and Xie that A = B [1]." Passive voice is not always bad! But it's more direct and clear (often) to write an actice sentence: "Wang and Xie showed that A = B [1]."  


#### Minor notes

* If using "use" works where you wanted to write "utilize", then use "use" instead.
* "upto" should be "up to"
* It is tempting to add capitalization to things but is often not needed.  
BAD: "the algorithm is $\epsilon$-Differentially Private", "we will use  Complex Analysis to solve this problem."   
GOOD: "the algorithm is $\epsilon$-differentially private", "we will use complex analysis to solve this problem."
* Look up what a "comma splice" is and avoid making them.

#### Mathematical writing

* See [this handy guide](https://math.mit.edu/~poonen/papers/writing.pdf).
* "Consider that $X > 0$" should be "Assume that $X > 0$"
* When citing a specific mathematical result, put in the reference to the specific result. For example:  
`Using the Weierstrass Approximation` `Theorem~\cite[Lemma 3.2]{Rudin}`
* Make sure
 
#### Citations and bibliographies

* Don't use citations as nouns.    
BAD:  "In [1], it was shown that A = B."
GOOD:  "Shah et al. [1] showed that A = B."
* Don't start sentences with a citation.  
BAD: "[1] showed that A = B."  
GOOD: "Shah et al. [1] showed that A = B."
* Keep a clean and consistent bibliography
  * Make sure all authors are listed. Check to make sure you have all accents in names! That is part of spelling the name correctly.
  * Either abbreviate **all** journal/conference titles or write all of them out in full.
  * Check titles for proper nouns! Unless you write "{Gaussian}" or "{G}aussian", LaTeX will render the it as "gaussian." This also holds for acronyms, so "{PCA}" and "{fMRI}" not "PCA" and "fMRI". 
  * Don't use "Signal Processing, IEEE Transactions on" but instead use "IEEE Transactions on Signal Processing"
  * Make sure you get page numbers if there are any: many publishers will ask you to put them in anyway so doing it ahead of time saves time later.
  * By default sure you include a URL in the BibTeX. They can be removed later if you need the space.
  * [Follow Prof. John D. Owens's advice](https://www.ece.ucdavis.edu/~jowens/biberrors.html)



## LaTeX

LaTeX is supposed to format things for you -- don't use manual line breaks like `\\` in running text unless you absolutley have to. You can often specifiy hyphenations in the preamble if you need to let LaTeX break lines.

Don't worry about issues like page length and so on until the paper is written -- it's a waste of time to hack around with stuff like that until you are on final edits cleaning things up. So don't evern put in things like `\vspace{-1cm}` or things like that to save space.

### Common LaTeX Errors to avoid

Here are some general tips to start out:

* [JDO's common errors](https://web.ece.ucdavis.edu/~jowens/commonerrors.html)
* [Eddie Kohler's advice](https://www.read.seas.harvard.edu/~kohler/latex.html)


### Mathematical writing

#### Notation and macros

Setting up good notation is hard! Sometimes you get halfway through writing something up and realize your notation is terrible and you have to switch all `x_i` to `z_i` for example. One thing that you can do to be more systematic and use macros to set notation for variables based on their meaning, so for example using `\newcommand{\loss}{\ell}` might save time if you decide to switch from using `\ell` for your loss function to using `f`.

Since LaTeX is used by so many different research communities, it's also helpful to define macros for your particular sub-area. For example, setting up a macro for Kullback-Leibler divergence can make equations a bit easier to read in the markup. The directory here has a set of basic macros which can be useful as a starting point, see `macros.tex`.

All things being equal, it's better to have an inset equation than an equation in running text.  It makes things a lot easier to read.

#### Miscellaneous tips and tricks

* Don't use the `equation` or `eqnarray` environments. Use `align` instead.  If it's an IEEE paper you can (should?) use `IEEEeqnarray`.  See the documentation for `IEEEeqnarray` if you like.

* Become familiar with the following environments which will save you a lot of anguish over using the `array` environment. 
	* `bmatrix`, `pmatrix`
	* `cases`

* Use auto-sizing delimiters like `\left[` and `\right]`. This statement might be slightly controversial but I stand by it. You want your equations to look nice and readable -- having parentheses that are too small makes things harder to understand.

* Remember to punctuate equations. Inline equations should be treated as if they are in running text.


### Making your LaTeX more readable

While using `Lyx` or `Overleaf` may make it seem like LaTeX can be done in a WYSIWYG manner, editing LaTeX is best done in the code, and you can do a lot to help yourself make the code more readable and hence easier to read/write.

#### Macros

Use macros to help you avoid pain when you (inevitably) discover there is a better notation for the problem you are trying to describe.  Examples of useful general macros that I use:

```
\def\mbf{\mathbf}
\def\mc{\mathcal}
\def\msf{\mathsf}
\newcommand{\norm}[1]{\left| #1 \right|}
\newcommand{\ip}[2]{\left\langle #1, #2 \right\rangle}
\newcommand{\diag}{\mathop{\mathrm{diag}}\nolimits}
\def\defeq{ \stackrel{\Delta}{=} }
\newcommand{\field}[1]{\mathbb{#1}}
\newcommand{\R}{\field{R}}
\newcommand{\argmax}{\mathop{\mathrm{argmax}}}
```

Using macros will save you a ton of time and also will make your LaTeX easier to read.  

#### Whitespace and pretty printing

LaTeX is insensitive to a lot of whitespace, so you can make your code easier to read/write/edit if you try to format it.  Therefore something like:

```
So we can see $$C(x,y)= \begin{cases} 
x^2 y & x < y \\ x^3 y^2 & x \ge y 
\end{cases}$$ yields the optmal tradeoff.
```

Is better as

```
So we can see
  \begin{align}
  C(x,y)= 
  	   \begin{cases}
	   x^2 y      &      x < y \\ 
	   x^3 y^2      &      x \ge y 
	   \end{cases}
  \end{align}
```
  
These two will look the same, but the latter is easier to read and edit. This is a matter of taste, but if you are writing with other people (e.g. your advisor) it helps to make the code easier to read.


### References and citations

* BibTeX and citation best practices
	* Use BibDesk (Mac) or JabRef (Windows) or a related tool
	* Possibly think of switching to BibLaTeX (may not be good for IEEE though)

* When referring to theorems, sections, etc, capitalize them.   
BAD: "we use theorem \ref{thm:upperbound} from section \ref{sec:bounds}"   
GOOD: "we use Theorem \ref{thm:upperbound} from Section \ref{sec:bounds}" 
	
#### Internal references

Use `\label` and `\ref` for internal references -- don't use static equation numbers. Use `\eqref{foo}` instead of `(\ref{foo})`.


## The Thesis

The thesis/dissertation is what you produce at the end of your Ph.D. as public proof that you have advanced human knowledge in some area through the work you have done in the last few years. It also is evidence that 
you have become an expert in an area of study. 

Some fields/advisors believe that it is ok to have a "staple thesis": just staple three papers together and turn it in. Sometimes this is literal -- an economics thesis I saw from MIT even restarted page numbers with each chapter and had separate bibliographies per chapter. However, a more conventional approach is to treat the thesis as a *synthesis* and *more fully explained* version of your research work. Not every paper of yours has to be crammed into the thesis.

Think of the thesis as being read by a student with a Masters who wants to work in this area. Your thesis should give them a good sense of:

* *What is the general state of known results and how did this area come about?* You want to both address the history of the field/problem and the specific recent advances to properly contextualize your own contribution. This is a more comprehensive and deeper literature review than you can plausibly fit into a paper. A good literature review is itself a research contribution: the student who reads your thesis next will really get a good sense of the field.
* (add more here)


### Advice when it comes time to write

**NEEDS TO BE WRITTTEN**

#### Common thesis mistakes

* Check everywhere that you have "chapter" instead of "paper". For example, "in this paper we show..." should become "in this chapter we show..."
* Thesis pages are wider than journal/conference paper columns: you don't need to break equations weirdly to fit (as often). This is a danger when you cut-and-paste from the journal/conference paper.
