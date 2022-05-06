# MathSemantics.sty

[![documentation](https://badgen.net/badge/documentation/pdf/green)](https://ronnybergmann.net/MathSemantics.sty/mathsemantics-documentation.pdf)
![LaTeX](https://badgen.net/badge/language/LaTeX/blue)
[![GitHub license](https://badgen.net/github/license/kellertuer/MathSemantics.sty)](https://github.com/kellertuer/MathSemantics.sty/blob/master/LICENSE) 


This LaTeX package `mathsemantics.sty` provides both syntactic and semantic helpers to typeset math in LaTeX. The syntactic layer eases typesetting of formular in general, while the semantic layer provides commands like `\inner{x}{y}` to unify
 typesetting of inner products. These not only unify typesetting of math formulae but also allow to easily adapt Notation if a user prefers to.
The semantic layer is split into topics.

## Example

Instead of always writing

```latex
\lVert x \rVert
```

for the norm and maybe having to manually increase _both_ delimiters for example in

```latex
\Bigr\lVert \frac{x}{2} \Bigr\rVert
```

with the commands from this package this simplifies to

```latex
\norm{x}
```

and

```latex
\norm[Big]{\frac{1}{2}}
```

For a comprehensive overview over all commands, see the [mathsemantics-documentation.pdf](https://ronnybergmann.net/MathSemantics.sty/mathsemantics-documentation.pdf).
