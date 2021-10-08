# Get your LaTeX files compiled and released on GitHub

This composite action should provide an all-in-one solution for having your LaTeX documents compiled and published.

```yaml
name: Build LaTeX and deploy on GitHub Releases
on:
  push:

jobs:
  Setup-Compile-Deploy:
    runs-on: ubuntu-latest
    steps:
      - env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        uses: DanySK/compile-and-publish-all-latex@master
```

Maybe pick the latest version instead of `master`...
