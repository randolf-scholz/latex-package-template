# CONTRIBUTING

[DEVELOPMENT INSTALL](#development-installation) | [RUNNING TEST](#running-tests) | [RUNNING LINT](#running-lint)

## Development Installation

The following dependencies are needed

- Working, recent $\LaTeX$ installation, including `latexmk`, `chktex` and `lacheck`.
- `pre-commit` <https://github.com/pre-commit/pre-commit>
- `just` command runner <https://github.com/casey/just>

I recommend installing these using `uv` (<https://github.com/astral-sh/uv>)

```bash
uv tool install pre-commit
uv tool install rust-just
git clone https://github.com/randolf-scholz/latex-package-template.git
cd latex-package-template
```

## Running Tests

This one-liner should run all tests:

```bash
just test
```

## Running Lint

```bash
pre-commit run -a
```
