# Contributing to `MathSemantics.sty`

First, thanks for taking the time to contribute.
Any contribution is appreciated and welcome.

The following is a set of guidelines to [`MathSemantics.sty`](https://github.com/kellertuer/MathSemantics.sty).

- [Contributing to `MathSemantics.sty`](#contributing-to-mathsemanticssty)
  - [I just have a question](#i-just-have-a-question)
  - [How can I file an issue?](#how-can-i-file-an-issue)
  - [How can I contribute?](#how-can-i-contribute)
    - [Add a missing command](#add-a-missing-command)
    - [Provide a new abbreviation or a name](#provide-a-new-abbreviation-or-a-name)
    - [Provide a new command](#provide-a-new-command)
    - [Code style](#code-style)

## I just have a question

The developers can most easily be reached in the GitHub Discussions at <https://github.com/kellertuer/MathSemantics.sty/discussions>

## How can I file an issue?

If you found a bug or want to propose a feature, we track our issues within the [GitHub repository](https://github.com/kellertuer/MathSemantics.sty/issues).

## How can I contribute?

### Add a missing command

If you have a semantic command, and abbreviation or a syntactic sugar that fits this package, feel free to add it. contribution.

### Provide a new abbreviation or a name

Abbreviations are all defined in `mathsemantics-abbreviations.sty`.
They are stored grouped by language and ordered alphabetically by command. Remember to also add a line in the Abbreviations section in the `mathsemantics-documentation.tex`

### Provide a new command

Since commands might be a little complex from time to time, we often use `\NewDocumentCommand` to define them. Please remember to add a documentation in the source code above the command.

Usually within a file (like `mathsemantics-semantic.sty` or `mathsemantics-manifold.sty`) first commands are defined, then math operators and symbols.

If you define a command that uses a symbol, provide that as a command as well, so it can easily be changed without redefining the whole (maybe complicated) command. One example is the command `\geodesic` and the `\geodesicSymbol`.

Remember to add an entry in the corresponding section in the documentation as well. Such an entry should explain all possible parameters, also the optional one. It should also provide an example usage of every parameter/setting that can be used. There is both a `\codeExample` as well as a `\mathCodeExample` example command that take one argument, which is both rendered as code and its resulting look.

### Code style

- the first optional parameter `[]` should usually be used to scale brackets appearing in a command and maybe also internal elements, like the `\mid` in `\setDef`.
- Commands are written in `CamelCase`, where the first letter might or might not be capitalised depending on the context
- The syntax helpers (Section 4.2 in the documentation) might be useful when parts should be enclosed in parenthesis or other delimiters
- For every command, the goal should be that the resulting mathematics is easier readable afterwards.
