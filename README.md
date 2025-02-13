# latex-package-template

Template for LaTeX packages

[INSTALLATION](#installation) | [USAGE](#usage) | [CONTRIBUTING](CONTRIBUTING.md)| [CHANGELOG](CHANGELOG.md) | [LICENSE](LICENSE)

## Installation

**Global Install:** Copy the content of `src` into your `TEXMFHOME` directory.

```bash
cp -r src/* $(kpsewhich -var-value TEXMFHOME)/tex/latex/
```

**Local Install:** Add as a submodule to your project, link the content of `src` to your project's local `texmf` directory.

```bash
mkdir -p my_project
cd my_project
git init
mkdir -p texmf/tex/latex
```

```bash
REPO='https://github.com/randolf-scholz/latex-package-template.git'
NAME=$(basename $REPO .git)
mkdir -p third_party
git submodule init
git submodule add "$REPO" "third_party/$NAME"
ln -sr "third_party/$NAME/src/"* "texmf/tex/latex/"
```

## Usage

Provides the [`\HelloWorld`](docs/features.md#hello-world) command.

**Example:**

```tex
\documentclass{article}
\usepackage{examplepkg}

\begin{document}
\HelloWorld
\end{document}
```
