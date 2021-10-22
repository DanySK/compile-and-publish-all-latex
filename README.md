# Get your LaTeX files compiled and released on GitHub
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex?ref=badge_shield)


This composite action should provide an all-in-one solution for having your LaTeX documents compiled and published.

```yaml
name: Build LaTeX and deploy on GitHub Releases
on:
  push:

jobs:
  Setup-Compile-Deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: DanySK/compile-and-publish-all-latex@master
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```

Maybe pick the latest version instead of `master`...


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FDanySK%2Fcompile-and-publish-all-latex?ref=badge_large)