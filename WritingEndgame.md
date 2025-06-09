## Final steps for finishing a manuscript

Ok so you've finished your writeup for a paper (conference or journal). Remember -- people will see a paper with your name on it and make assumptions about who you are. If your paper is confusing and doesn't proceed in a clear and ordered way then they will think your thinking is messy. If your bibliography has typos and looks like you didn't really look at it they will think that you either didn't even read the papers your reference or they will think that your paper will also be full of typos and mistakes.

Once you get the ideas in the right order, the technical material written, and the major issues out of the way, it may come time to "polish" the manuscript. What I call "polishing" is an iterative process to edit and improve the manuscript. 


### Final checks

When you are going to submit something it helps to go through through the manuscript several times to check one last time for the small issues. Being systematic about this will take less time and catch more bugs. You can do complete checks over the document for each of these things one by one, so a check for typos, for citations, for bibliography, for math formatting, etc. Focusing on one issue per go-through is better so that you don't miss things from context-switching.

The major things to check for (one pass through the manuscript for each) are:

1. **Typos**: there are now pretty decent spell check tools for LaTeX. The only downside is that dictionaries generally don't have lots of the technical words, so you might have to click through every time it flags "nonparametric" and so on.
2. **Grammar**: read the paper *backwards*, sentence-by-sentence or paragraph-by-paragraph. This helps you focus on each sentence individually to make sure it's correct. You can also see if the logic flows correctly.
3. **Notation consistency**: you should have written the manuscript using macros for the major notation if you followed the earlier advice. Do a check for notation consistency by making sure you used the macro everywhere and double check the macros to make sure the notation is what you want.
* **Bibliography**: check that the bibliography looks consistent and correct. Make sure you have all the required fields for bibliography entries. IEEE has [a guide about what entries are needed](https://journals.ieeeauthorcenter.ieee.org/wp-content/uploads/sites/7/IEEE_Reference_Guide.pdf) which is a reasonable starting point.

You should also check for:

* **Citations as nouns**: search for `\cite{}` commands and make sure you're not treating any of them as nouns. See below for more details.
* **Math formatting**: check that equations have autosizing delimiters and are punctuated correctly. Check that there are not extra blank lines before/after equations.

#### Citations and bibliographies

[Follow Prof. John D. Owens's advice](https://www.ece.ucdavis.edu/~jowens/biberrors.html). IEEE has [guidance on what fields are needed](https://journals.ieeeauthorcenter.ieee.org/wp-content/uploads/sites/7/IEEE_Reference_Guide.pdf) as well.

* Don't use citations as nouns.    
BAD:  "In [1], it was shown that A = B."
GOOD:  "Shah et al. [1] showed that A = B."
* Don't start sentences with a citation.  
BAD: "[1] showed that A = B."  
GOOD: "Shah et al. [1] showed that A = B."
* When citing a specific mathematical result, put in the reference to the specific result. For example:  
`Using the Weierstrass Approximation` `Theorem~\cite[Lemma 3.2]{Rudin}`
* Keep a clean and consistent bibliography
  * Make sure all authors are listed. Check to make sure you have all accents in names! That is part of spelling the name correctly.
  * Either abbreviate **all** journal/conference titles or write all of them out in full.
  * Check titles for proper nouns! Unless you write "{Gaussian}" or "{G}aussian", LaTeX will render the it as "gaussian." This also holds for acronyms, so "{PCA}" and "{fMRI}" not "PCA" and "fMRI". 
  * Don't use "Signal Processing, IEEE Transactions on" but instead use "IEEE Transactions on Signal Processing"
  * Make sure you get page numbers if there are any: many publishers will ask you to put them in anyway so doing it ahead of time saves time later.
  * By default sure you include a DOI or URL in the BibTeX if available. They can be removed later if you need the space.

**ArXiV Papers**: Google Scholar and even ArXiV itself uses the `@misc` type for ArXiV preprints. I think that `@techreport` looks a bit nicer but `@misc` is fine. Just make sure you pick one and stick with it.


### Making things fit

You will often end up in the situation where your paper is anywhere from a few paragraphs to several pages over the limit for wherever you are submitting. The question is how do you make it all fit?

Things **not** to do:

* Do not use `\vspace{-1mm}` or any sort of "negative" spacing. This is all manual hacking and should be avoided: let LaTeX do the layout, not you. That's the whole point of logical formatting.

The trick is to go systematically to make things fit. Work from the end of the document forward.

* Move material to the appendix or supplementary material.
* Check if you have too much "navigation" text. Conference papers are short and do not need an "organization of this paper" section. Having text at the end of sections saying what is coming next or text at the start of a section summarizing the section is nice from a reading perspective but is not always necessary. It's easy to go too far in this direction, but often this is filler.
* Edit your sentences to make them simpler. See some of the writing/editing tips and advice for this. There are a lot of "unnecessary words" that we all use when writing. For example, this document you are reading is too wordy and could uuse some editing. Read the writing guides for tips and tricks!
* Move (some) equations in-line. It's easy to go overboard on this! Any time you want to move an equation from display mode to in-line, ask yourself how important that equation is and whether it will help the reader to see it displayed/centered versus in-line.
* Manipulate figures. Shrinking figures is a way to get more space but make sure they are still legible/readable! You might want to make the lines in the plot thicker to be easier to read. Sometimes you might have an illustrative figure which helps the reader figure out what is going on: those are good targets for moving to an appendix or removing from the paper, especially if the space-to-benefit ratio is high.
