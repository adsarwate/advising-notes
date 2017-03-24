# Advising notes


## Some skills to acquire

* How to read a paper
* How to review a paper
* How to do a literature search
* How to write a literature review
* Critical reading
* Talks
	* Conference talks
	* Qualifying/proposal talks
	* Seminar talks


## Software and tools

* git
* website
* mendeley?
* python
* other languages

## Writing tips

General writing advice:

* Writing is hard! It is 99% rewriting.

### Getting started with writing

* Mind maps
* Outlining
* Avoiding censoring
* Being verbose

### Editing and improving your writing


* [Common errors](http://www.cs.columbia.edu/~hgs/etc/writing-bugs.html)

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

While using `Lyx` or `Overleaf` or `ShareLaTeX` may make it seem like LaTeX can be done in a WYSIWYG manner, editing LaTeX is best done in the code, and you can do a lot to help yourself make the code more readable and hence easier to read/write.

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
	* [Follow Prof. John D. Owens's advice](https://www.ece.ucdavis.edu/~jowens/biberrors.html)

In addition, here are a few more tips.

#### Internal references

Use `\label` and `\ref` for internal references -- don't use static equation numbers. Use `\eqref{foo}` instead of `(\ref{foo})`.



