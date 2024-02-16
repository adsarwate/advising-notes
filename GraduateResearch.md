# Becoming a graduate researcher

**THIS IS BEING SPLIT INTO MULTIPLE FILES, stuff will vanish from here beware!!!**





### Editing and rewriting

There is a ton of advice out there on editing and writing. Here are a few references which I think are extremely helpful:

* [Common errors](https://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)
* Howard S. Becker, Writing for Social Scientists, University of Chicago Press, 2007.  
You may think that this is not a book engineers need to read but it has lots of great advice about the writing process, especially in the first few chapters.

For some very specific advice (big and small) regarding mathematical writing, see the tips section of [this overleaf template](https://www.overleaf.com/read/hczfttksjhqs)


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
