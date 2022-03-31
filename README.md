# Pyright PR Annotator

## Usage

Annotate pull requests with pyright errors detected during CI.

Note: This doesn't install or run pyright, it just sets up the PR annotations.

### Example workflow

```yaml
name: My Workflow
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@master

      - name: Add pyright annotator
        uses: pr-annotators/pyright-pr-annotator@master

      - name: Run pyright
        uses: jakebailey/pyright-action@v1
```
