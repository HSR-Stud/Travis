# Travis Configuration

## Overview

Travis is configured to build with XeLaTeX

- `texliveonfly` to try to automatically needed packages to build the document
- `latexmk` runs the LaTeX compiler however many times it is needed to get everything right (references, bibliography, etc)

To configure correctly Travis you need to change the following variable in `.travis.yaml`

```yaml
env:
  global:
    - TEX_MAIN=<your document>.tex
```

## When Travis fails because a package is missing

If `texliveonfly` fails to detect a needed package and the compilation hangs, you may need to manually add your package to `.travis/texlive/texlive_packages`

## References

- [https://github.com/PHPirates/travis-ci-latex-pdf]
- [https://malramsay.com/post/compiling_latex_on_travis/]
- [https://www.ctan.org/tex-archive/support/texliveonfly]
- [https://tex.stackexchange.com/questions/398830/how-to-build-my-latex-automatically-using-travis-ci]
- [https://docs.travis-ci.com/user/deployment/script]

