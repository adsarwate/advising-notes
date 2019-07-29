# Becoming a graduate researcher

##### an idiosyncratic take by Anand D. Sarwate

These are some notes and miscellaneous items about skills and tips for success in graduate school (and beyond!). It is (a) not comprehensive and (b) very idiosyncratic. Things I'm not going to talk about:

* what classes to take
* how to pass various exams

## Getting started: look like a researcher, not an undergrad

Since your goal is to publish new research discoveries, you have to start thinking of yourself as having a "public image" as a researcher. This means you have to create a way for other researchers (or potential employers) to find you and learn more about what you are working on. The last thing you want is for people to search for your name and turn up nothing or worse, a bunch of links to different people with the same name with embarassing social media presences.

A checklist:

* Create a homepage
* Make git repo
* Consider your social media presence
* Update your profile on LinkedIn
* Create an ORCID

You can do all of these in half an afternoon (at least a minimum). There is really no excuse to not doing this **immediately**.

### Create a homepage

You should create a homepage for yourself. Why? That way you have a place to put your CV, links to projects and code, a description of your research, and other public-facing information about yourself. You don't have to list hobbies or the books you read or anything else that you don't feel like sharing. But having a homepage gives people wanting to know more about your research someplace to go.

You can either host the website on a department or university server or make a site on Google Sites or some other web-based service.

* An institutional website means you probably have to edit the HTML yourself, but there are lots of templates out there. Perhaps the most famous is [jemdoc](https://jemdoc.jaboc.net). It also has the advantage
* Third-party hosting means your page will not die when you graduate but it (usually) gives you a little less control and makes you "less obviously" affiliated with your university.

### Make a git repo

It is very important to have a public repository of code from projects you have worked on. Perhaps you already have a git account on [GitHub](https://www.github.com/) or [GitLab](https://www.gitlab.com/): good for you! There are lots of reasons to have a homepage:

* If you write code for an algorithm you developed or a simulation from a paper, you should create a repo for the paper and post the code (including preprocessing) and data (or a link to the data if it's a public data set). This is part of doing reproducible research.
* If you apply for an internship, companies will look at your git repos. If you have nothing there, they will think you have no skills: it looks bad! If you have no papers yet but some code from class projects, put up the code and project there. This shows that you know how to do things.
* If you get a job in industry, chances are you will have to use git. You should be aware of how it works and how to use it in order to be more employable.

Make sure you link to your git account from your homepage!
 
### Social media

Social media is currently a totally optional thing -- lots of prominent researchers do not have Twitter accounts. However, if it is something you are comfortable with, you might consider creating a Twitter account to engage with other members of the academic community (and the public more broadly). The downsides are standard: social media can be a total waste of time and attention. The upsides are that you might get a better sense of what kind of research is interesting to people/generates a lot of attention.

If you already have a Twitter handle, keep in mind that people who read your papers will automatically connect your Twitter handle with your role as a researcher. This is a hazard

### Update LinkedIn

Even if it's not clear how much it helps you, it doesn't really hurt you to have a profile up. Employers will look you up on LinkedIn, including people looking for potential interns. This is especially true of managerial level folks who are less interested in poking through your github. Create a profile there and make sure the information is current (including the homepage you just made).

A great resource for understanding job-related things, how to present yourself in interviews, and so on, is the [Ask a Manager](https://www.askamanager.org/) blog.

### Create an ORCID

Many publication venues are requring authors to link their papers with their ORCID. You can create one at [https://www.orcid.org/](https://www.orcid.org/).

## Some skills to acquire

There are a lot of different concrete skills that you (should) develop as a graduate student. A lot of these have to do with successfully grappling with the vast amount of research that already exists: how to read it, how to evalute it critically, how to organize and summarize it, and how to present it.

### How to read a paper

There is already lots of advice on how to read papers:

**to be written**

### How to do a literature search

**to be written**

### How to write a literature review

**to be written**

### How to review a paper

Chances are, once you have gotten a reasonable handle on research in an area and 

There is already lots of advice on how to write a review:

**find from old emails**

### How to give a talk

There is infinite advice out there on how to give good talks, as well as some pretty funny advice about how to not to give talks

#### Conference talks
#### Group meeting/lab talks
#### Seminar talks



## Software and tools

In addition to having a homepage and a git repo, there are a number of other pieces of software which are important to learn how to use.

### Bibliography management

You should end up reading a **lot** of papers in grad school. You need to figure out how to organize them! There are quite a few tools out there:

* Zotero: an open-source bibliography management tool with web browser plug-ins so you can create an entry from data scraped from the paper's website.
* Mendeley: I used to like this, but they were bought by Elsevier, which is evil, so I no longer recommend it.
* Many BibTeX or BibLaTeX managers (e.g. BibDesk on Mac OS) have a "notes" feature or something where you can type in some quick notes associated to the bib entry.

It helps to have some sort of "diary" or other way of keeping a log of what you've been reading and what the main points of the paper were, things that were interesting or confusing, and things that you might want to follow up on. For the last thing, it could be some problem the paper left unanswered (maybe you can answer it) or some new analysis/technique you might want to learn, or just that you need to cite this paper when working on this problem.

### Programming

If you are an EE student, chances are you have done a lot of your programming in MATLAB. While lots of places still use MATLAB, you are better off learning Python, and particular using `numpy` and `scipy` for simulations. If you are doing large-scale nachine learning (e.g. deep learning) you might want to learn how to use [PyTorch](https://pytorch.org) or [TensorFlow](https://www.tensorflow.org/). Download [Jupyter](https://jupyter.org) so you can make interactive Python `.ipython` notebooks -- this is a good way to keep track of code and notes, since the notebooks support LaTeX markup.

Another language you can learn (especially if you think you might be engaging seriously with the statistics literature) is `R`. The syntax is very similar to MATLAB (and in particular matrix multiplication, which is ugly in Python, is more MATLAB-like in `R`). There is a very active open-source development base for `R` and many statistics papers come with an `R` package that you can install and use to test/apply the methods.

Knowing Python, `R`, and MATLAB are a good start, but if you want to do more serious software development, learning C# or C++ or another "real" (compiled) language is not a bad idea.

Why am I so anti-MATLAB? It's expensive, not that fast, and industry is moving away from it. Switching to Python is not hard, once you overcome the psychological barrier of having to learn another language.


## Computational Experiments





## Writing tips

General writing advice:

* Writing is hard! It is 99% rewriting.

### Getting started with writing

* Mind maps
* Outlining
* Avoiding censoring
* Being verbose

### Editing and rewriting

There is a ton of advice out there on editing and writing. Here are a few references which I think are extremely helpful:

* [Common errors](https://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)
* Howard S. Becker, Writing for Social Scientists, University of Chicago Press, 2007.  
You may think that this is not a book engineers need to read but it has lots of great advice about the writing process, especially in the first few chapters.


#### Starting out

When you sit down to formally write up your results into something that looks like a paper, it's time to get a bit more organized and systematic. You might be starting from some other informal writeup in LaTeX, or just handwritten notes, or just little snippets and fragments from an email thread. Regardless of what you have so far, *make a fresh document*. 

I learned many of the rules of mathematical writing from this handout from when I was an undergradute:

* [Writing a Math Phase Two Paper](http://web.mit.edu/18.704/www/piiUJM2.pdf). There is an HTML [(older version)](http://web.mit.edu/mathp2/www/piil.html)

Mathematical writing is its own skill and it not the same writing that you would do on a homework or exam. This is often the hardest thing for graduate students to learn. It takes *practice*.

If you plan to submit to a conference, use the template from the conference website. Templates change over time, sometimes in small ways, and the last thing you want is to have the server reject your PDF for some formatting violation caused by you using the previous year's template (this has happened to me).

Finally, remember that when you sit down to write, you're going to be doing a lot of editing and rewriting afterwards. Resist the urge to try and apply constraints or formatting hacks: save it for the editing stage. "Making it fit into the page limits" is something you can work on *after* your ideas are cleanly and clearly written.

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
* Edit your sentences to make them simpler. See some of the writing/editing tips and advice for this. There are a lot of "unnecessary words" that we all use when writing. This document is replete with them.
* Move (some) equations in-line. It's easy to go overboard on this! Any time you want to move an equation from display mode to in-line, ask yourself how important that equation is and whether it will help the reader to see it displayed/centered versus in-line.
* Manipulate figures. Shrinking figures is a way to get more space but make sure they are still legible/readable! Sometimes you might have an illustrative figure which helps the reader figure out what is going on: those are good targets for moving to an appendix or removing from the paper, especially if the space-to-benefit ratio is high.

### Specific common issues

There are a couple of issues which are specific to technical writing. Here are some major ones to consider.

#### Grammar and sentence structure

* Many writers think that long, complicated sentences are more sophisticated. In reality, they are harder to read. You can introduce more complex sentence structure later. For the early drafts, just stick to short and simple sentences.
* Passive voice. You will read a lot of technical writing that is written in passive voice. For example: "it was shown by Wang and Xie that A = B [1]." Passive voice is not always bad! But it's more direct and clear (often) to write an actice sentence: "Wang and Xie showed that A = B [1]."  


#### Minor notes

* If using "use" works where you wanted to write "utilize", then use "use" instead.
* "upto" should be "up to"
* It is tempting to add capitalization to things. Capitalization should be reserved for proper nouns and in particular, should not be used when talking about a definition of some mathematical property.  
BAD: "the algorithm is $\epsilon$-Differentially Private", "we will use  Complex Analysis to solve this problem."   
GOOD: "the algorithm is $\epsilon$-differentially private", "we will use complex analysis to solve this problem."
* Look up what a "comma splice" is and avoid making them.

#### Mathematical writing

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
  * Check titles for proper nouns! Unless you write "{Gaussian}" or "{G}aussian", LaTeX will render the it as "gaussian." This also holds for acronyms, so "{PCA}" and "{fMRI}" not "PCA" and "fmri". 
  * Don't use "Signal Processing, IEEE Transactions on" but instead use "IEEE Transactions on Signal Processing"
  * Make sure you get page numbers if there are any: many publishers will ask you to put them in anyway so doing it ahead of time saves time.
  * By default sure you include a URL in the BibTeX. They can be removed later.
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
  
These two will look the same, but the latter is easier to read and edit.


### References and citations

* BibTeX and citation best practices
	* Use BibDesk (Mac) or JabRef (Windows) or a related tool
	* Possibly think of switching to BibLaTeX (may not be good for IEEE though)
	
#### Internal references

Use `\label` and `\ref` for internal references -- don't use static equation numbers. Use `\eqref{foo}` instead of `(\ref{foo})`.


## The Thesis

The thesis/dissertation is what you produce at the end of your Ph.D. as public proof that you have advanced human knowledge in some area through the work you have done in the last few years. It also is evidence that 
you have become an expert in an area of study. 

Some fields/advisors believe that it is ok to have a "staple thesis": just staple three papers together and turn it in. Sometimes this is literatl -- an economics thesis from MIT even restarted page numbers with each chapter. However, a more conventional approach is to treat the thesis as a *synthesis* and *more fully explained* version of your research work. Not every paper of yours has to be crammed into the thesis.

Think of the thesis as being read by a student with a Masters who wants to work in this area. Your thesis should give them a good sense of:

* *What is the general state of known results and how did this area come about?* You want to both address the history of the field/problem and the specific recent advances to properly contextualize your own contribution. This is a more comprehensive and deeper literature review than you can plausibly fit into a paper. A good literature review is itself a research contribution: the student who reads your thesis next will really get a good sense of the field.


### Advice when it comes time to write


#### Common thesis mistakes

* Check everywhere that you have "chapter" instead of "
* Thesis pages are wider than journal/conference paper columns: you don't need to break equations weirdly to fit (as often). This is a danger when you cut-and-paste from the journal/conference paper.
