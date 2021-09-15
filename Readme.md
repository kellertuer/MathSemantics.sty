# Mathemantics.sty

This LaTeX package `mathemantics.sty` provides both syntactic and semantic helpers to typeset math in LaTeX. The syntactic layer eases typesetting of formular in general, while the semantic layer provides commands like `\inner{x}{y}` to unify
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
\norm[Big]{x}
```

For a comprehensive overview over all commands, see the `mathemantics-documentation.pdf`.