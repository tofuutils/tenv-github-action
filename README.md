# tenv-github-action


## Workflow example
*  Add the step into your github
```
name: "Workflow Example"

on:
  push:
    branches:
      - "main"

jobs:
  example:
    runs-on: ubuntu-20.04
    steps:
      - uses: tofuutils/tenv-github-action@main
        with:
          tool_name: terraform
          tool_version: 1.5.7
      - name: Test terraform
        run: terraform version

      - uses: tofuutils/tenv-github-action@main
        with:
          tool_name: tofu
          tool_version: 1.8.0

      - name: Test OpenTofu
        run: tofu version
```
