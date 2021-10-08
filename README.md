# Get your LaTeX files compiled and released on GitHub

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

# TODOS:

1. get https://github.com/renovatebot/renovate/pull/11533 merged
2. write action.yml
3. create a testing workflow:
  1. But HOW?
4. Update this readme 
