# Graduate Advising Notes

These are some notes and miscellaneous items about skills and tips for success in graduate school (and beyond!). It is (a) not comprehensive and (b) idiosyncratic.

## Some skills to acquire

There are a lot of different concrete skills that you (should) develop as a graduate student. A lot of these have to do with successfully grappling with the vast amount of research that already exists: how to read it, how to evalute it critically, how to organize and summarize it, and how to present it.

### How to read a paper

There is already lots of advice on how to read papers:

### How to do a literature search

### How to write a literature review

### Critical reading

### How to review a paper

Chances are, once you have gotten a reasonable handle on research in an area and 

There is already lots of advice on how to write a review:

### Talks

#### Conference talks
#### Qualifying/proposal talks
#### Seminar talks

## Looking more professional

Since your goal is to publish new research findings, you have to start thinking of yourself as having a "public image" as a researcher. This means you have to create a way for other researchers (or potential employers) to find you and learn more about what you are working on. The last thing you want is for people to search for your name and turn up nothing or worse, a bunch of links to different people with the same name.

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

## Software and tools

In addition to having a homepage and a git repo, there are a number of other pieces of software which are important to learn how to use.

### Bibliography management

You should end up reading a **lot** of papers in grad school. You need to figure out how to organize them! There are quite a few tools out there:

* Zotero: an open-source bibliography management tool with web browser plug-ins so you can create an entry from data scraped from the paper's website.
* Mendeley: I used to like this, but they were bought by Elsevier, which is evil, so I no longer recommend it

### Programming

If you are an EE student, chances are you have done a lot of your programming in MATLAB. While lots of places still use MATLAB, you are better off learning Python, and particular using `numpy` and `scipy` for simulations. If you are doing large-scale nachine learning (e.g. deep learning) you might want to learn how to use [PyTorch](https://pytorch.org) or [TensorFlow](https://www.tensorflow.org/). Download [Jupyter](https://jupyter.org) so you can make interactive Python `.ipython` notebooks -- this is a good way to keep track of code and notes, since the notebooks support LaTeX markup.

Another language you can learn (especially if you think you might be engaging seriously with the statistics literature) is R. The syntax is very similar to MATLAB (and in particular matrix multiplication, which is ugly in Python, is more MATLAB-like in R). There is a very active open-source development base for R and many statistics papers come with an R package that you can install and use to test/apply the methods.

Knowing Python, R, and MATLAB are a good start, but if you want to do more serious software development, learning C# or C++ or another "real" (compiled) language is not a bad idea.

Why am I so anti-MATLAB? It's expensive, not that fast, and industry is moving away from it. Switching to Python is not hard, once you overcome the psychological barrier of having to learn another language.

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

Once you get the ideas in the right order, the technical material written, and the major issues out of the way, it may come time to "polish" the manuscript. What I call "polishing" is an iterative process to 

When you are going to submit something it helps to go through through the manuscript several times to check one last time for the small issues. Being systematic about this will take less time and catch more bugs.

* *Spelling and grammar*: read the paper backwards, sentence by sentence (or paragraph by paragraph. This helps you focus on each sentence individually to make sure it's correct.
* *Bibliography*: check that the bibliography looks consistent (see below) and correct.
* *Math formatting*: check that equations have autosizing delimiters and are punctuated correctly.

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
`Using the Weierstrass Approximation Theorem~\cite[Lemma 3.2]{Rudin}`
* 
 
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


### Tips in writing math

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


