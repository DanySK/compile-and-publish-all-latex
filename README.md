# Get your LaTeX files compiled and released on GitHub
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex?ref=badge_shield)


This composite action should provide an all-in-one solution for having your LaTeX documents compiled and published on GitHub.

```yaml
name: Build LaTeX and deploy on GitHub Releases
on:
  push:

jobs:
  Setup-Compile-Deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: DanySK/compile-and-publish-all-latex@master
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```

Maybe pick the latest version instead of `master`...

> [!NOTE]  
> LaTeX is compiled with [DanySK/compile-latex-action](https://github.com/DanySK/compile-latex-action?tab=readme-ov-file#compile-latex-action), read its documentation to avoid pitfalls!

## Generating diffs

This action supports the generation of differential documents by wrappin [auto-latexdiff](https://github.com/DanySK/auto-latexdiff).
Diffs can be enabled by setting `diff-enable` to `true`.

## Available options

The following snippet launches the action with all parameters set to their default value.

```yaml
name: Build LaTeX and deploy on GitHub Releases
on:
  push:

jobs:
  Setup-Compile-Deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: DanySK/compile-and-publish-all-latex@master
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          # All the following parameters are optional, and these are their default values
          diff-enable: false
          diff-files: |
            **/*.tex
          diff-lightweight-tags: false
          diff-tag-regex: |
            .*
          publish-enable: true
```

## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex?ref=badge_large)
