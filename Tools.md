## Software and tools

In addition to having a homepage and a git repo, there are a number of other pieces of software which are important to learn how to use.

### Bibliography management

You should end up reading a **lot** of papers in grad school. You need to figure out how to organize them! There are quite a few tools out there:

* [Zotero](https://www.zotero.org/) helps manage papers and references (like iTunes for your research papers). It's ope-source There are browser plugins that let you grab the PDF and citation information from the website of a paper.
* Many BibTeX or BibLaTeX managers (e.g. BibDesk on Mac OS) have a "notes" feature or something where you can type in some quick notes associated to the bib entry.

If you read a paper and find it remotely interesting or helpful, get the bibliography entry for it. **NOTE:** Zotero, if you use it, will generate .bib files for use with LaTeX. Chances are that they will not be formatted properly and your bibliography will look messy when compile. So you need to manually fix those .bib entries.

There are many issues that come up in bibliographies: John Owens [has a whole webpage of them](https://www.ece.ucdavis.edu/~jowens/biberrors.html).

It helps to have some sort of "diary" or other way of keeping a log of what you've been reading and what the main points of the paper were, things that were interesting or confusing, and things that you might want to follow up on. For the last thing, it could be some problem the paper left unanswered (maybe you can answer it) or some new analysis/technique you might want to learn, or just that you need to cite this paper when working on this problem.

### Programming

If you are an EE student, chances are you have done a lot of your programming in MATLAB. I'm a bit anti-MATLAB because it's expensive, not that fast, and industry is moving away from it.

At the moment, you are better off learning [Python](https://www.python.org/) and getting familiary with `numpy`, `scipy` (and `scikit-learn`), and `pandas` (or `seaborne`). Python is [not a great language](https://medium.com/nerd-for-tech/python-is-a-bad-programming-language-2ab73b0bda5) from a programming languages standpoint. But at this point it's dominant. Just try not to get bad programming habits. Switching to Python is not hard, once you overcome the psychological barrier of having to learn another language.

* Most people I know use the [Anaconda](https://www.anaconda.com/products/distribution) distribution with the Spyder IDE. There are also people who hate Anaconda for various reasons.
* Other people use [Jupyter](https://jupyter.org) and do stuff in interactive Python `.ipython` notebooks -- this is a good way to keep track of work in progress and notes, since the notebooks support LaTeX markup.
* If you are doing large-scale nachine learning (e.g. deep learning) you will want to learn how to use [PyTorch](https://pytorch.org), [TensorFlow](https://www.tensorflow.org/), or [JAX](https://github.com/google/jax). 

Another language you can learn (especially if you think you might be engaging seriously with the statistics literature) is `R`. The syntax is very similar to MATLAB (and in particular matrix multiplication, which is ugly in Python, is more MATLAB-like in `R`). There is a very active open-source development base for `R` and many statistics papers come with an `R` package that you can install and use to test/apply the methods. `R` is also not a good programming language, but it's still pretty popular in the statistics community.

Knowing Python, `R`, and MATLAB are a good start, but if you want to do more serious software development, learning C# or C++ or another "real" (compiled) language is not a bad idea. People also like Rust. And Haskell. I'm not a programming languages expert.


### Figures

* [draw.io](https://draw.io/) is a very handy web-based tool for drawing simple figures. 
