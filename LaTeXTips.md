## Writing better LaTeX

The LaTeX system is designed to have the layout and rendering be done by the TeX engine and not you. So fiddling around with spacing manually is 

This is a document collecting some tips on writing (both mathematical writing and LaTeX tips/tricks.

### Macros and packages that are useful

* [formatting.tex](LaTeX/formatting.tex) has a bunch of packages that are included for use in this template.
* [macros.tex](LaTeX/macros.tex) has macros which you might find useful, like using `\mbf` and `\mc` for ``\mathbf` and `\mathcal`, or custom functions like `\prob{X \in \mc{A}}` for probabilities and `\expect{X^2}` for expectations. There are also conditional distributions `\condP{A}{B}` and expectations `\condE{Y}{X}`, as well as inner products `\ip{\mbf{x}}{\mbf{y}}`,  matrix norms: `\matnorm`. Check out the file for more.
* There are autosizing delimiters which are starred versions of the paired delimiters. Here's an example:
>		\begin{align}
>		\E{ f\parens*{ \bigcup_{i=1}^{N} \mc{X}_i } 
>			- \norm*{ \sum_{i=1}^{n} X_i }_{L^1} } 
> 		\ge 0.
>		\end{align}
* For functions with names like "Diam", it looks a bit nicer to typeset them like $\sin$ or $\cos$ (i.e. not italicised). Some functions like $\Var(\cdot)$ are already defined in the macros file. The best way to define a new command like this is
> 		\DeclareMathOperator{\Diam}{Diam} 

### Equation formatting

* It's better *not* to use the double dollar for equation environments (see [StackExchange](\url{https://tex.stackexchange.com/questions/503/why-is-preferable-to)  
* I am also not a big fan of `\[` and `\]` because it tends to make the code harder to read. I suggest sticking with `align`.
* I prefer `align` to `equation` and `eqnarray`. For numbered equations, it's easier to use `align` and not `align* and then put notag` to suppress numbers you don't want:
>		\begin{align}
>		f(t) 
>		&\le g(t) \notag \\
>		&= h(t) \notag \\
>		&\le M.  \label{eq:notag:example}
>		\end{align}
* Equations should be punctuated like sentences (so a comma or a period or nothing). At least, that's what I learned.
* Do not leave a blank line between the text and the equation because it will leave extra space. So do this:
>		Plugging in our formula for $\sigma$, we get
>			\begin{align}
>			\frac{3}{\gamma} n^{-1/2} \le 1.
>			\end{align}

* and not
>		Plugging in our formula for $\sigma$, we get
>
>			\begin{align}
>			\frac{3}{\gamma} n^{-1/2} \le 1
>			\end{align}	

* You may notice that I "pretty print" my code. I think this makes the code easier to read and issues with equations not rendering properly faster to debug. Nobody is charging you by the line number. If you want some visual separation in the code, putting a comment `%` can give you that space:
>		Plugging in our formula for $\sigma$, we get
>		%
>			\begin{align}
>			\frac{3}{\gamma} n^{-1/2} \le 1
>			\end{align}	

### References and labels

* You can use `\label` and `\ref` to avoid hard-coding references. Use `\eqref` for equation references and then it will automatically put the parentheses around the number.
* There is a package called `cleverref` which will automatically add the word in so that `\cref{sec:model}` would turn into `Section 2` and not just `2`. It's nice but sometimes doesn't play well with other packages.


