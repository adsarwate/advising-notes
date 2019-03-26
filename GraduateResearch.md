# Graduate Advising Notes

## Some skills to acquire

### How to read a paper

### How to review a paper

### How to do a literature search

### How to write a literature review

### Critical reading

### Talks

#### Conference talks
#### Qualifying/proposal talks
#### Seminar talks

## Looking more professional

Since your goal is to publish new research findings, you have to start thinking of yourself as having a "public image" as a researcher. This means you have to create a way for other researchers (or potential employers) to find you and learn more about what you are working on. The last thing you want is for people to search for your name and turn up nothing or worse, a bunch of links to different people with the same name.

### Create a homepage


### Make a git repo

### Social media

Social media is currently a totally optional thing -- lots of prominent researchers do not have Twitter accounts. However, if it is something you are comfortable with, you might consider creating a Twitter account to engage with other members of the academic community (and the public more broadly). The downsides are standard: social media can be a total waste of time and attention. The upsides are that you might get a better sense of what kind of research is interesting to people/generates a lot of attention.

## Software and tools

* website
* git
* bibliographic management
* programming: Python, R, MATLAB

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

* [Common errors](http://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)
* Howard S. Becker, Writing for Social Scientists, University of Chicago Press, 2007.  
You may think that this is not a book engineers need to read but it has lots of great advice about the writing process, especially in the first few chapters.

Once you get the ideas in the right order, the technical material written, and the 

### Specific common issues

There are a couple of issues which are specific to technical writing. Here are some major ones to consider.

#### Grammar and sentence structure

* Passive voice. You will read a lot of technical writing that is written in passive voice. For example: "it was shown by Wang and Xie that A = B [1]." Passive voice is not always bad! But it's more direct and clear (often) to write an actice sentence: "Wang and Xie showed that A = B [1]." 

#### Minor notes

* almost never use the word "utilize" when "use" would work just as well
* "upto" should be "up to"


#### Mathematical writing

* "Consider that $X > 0$" should be "Assume that $X > 0$"

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

LaTeX is supposed to format things for you -- don't use manual line breaks like \\ in running text unless you absolutley have to. You can often specifiy hyphenations if you need to let LaTeX break lines.

Don't worry about issues like page length and so on until the paper is written -- it's a waste of time to hack around with stuff like that until you are on final edits cleaning things up.

### Common LaTeX Errors to avoid

Here are some general tips to start out:

* [JDO's common errors](http://web.ece.ucdavis.edu/~jowens/commonerrors.html)
* [Eddie Kohler's advice](http://www.read.seas.harvard.edu/~kohler/latex.html)


### Tips in writing math

All things being equal, it's better to have an inset equation than an equation in running text.  It makes things a lot easier to read.

* Don't use the `equation` or `eqnarray` environments. Use `align` instead.  If it's an IEEE paper you can (should?) use `IEEEeqnarray`.  See the documentation for `IEEEeqnarray` if you like.

* Become familiar with the environments 
	* `bmatrix`, `pmatrix`
	* `cases`

* Use auto-sizing delimiters like `\left[` and `\right]`. This might be slightly controversial.

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
	

In addition, here are a few more tips.

#### Internal references

Use `\label` and `\ref` for internal references -- don't use static equation numbers. Use `\eqref{foo}` instead of `(\ref{foo})`.


