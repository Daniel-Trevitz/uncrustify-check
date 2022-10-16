# uncrustify-check

Opinionated GitHub action for style-checking code using [Uncrustify](https://github.com/uncrustify/uncrustify).

## Inputs
- `configFile` -- Path to Uncrustify configuration file.

# Setup
```
on: [ pull_request ]

jobs:
  cpp_style_check:
    runs-on: ubuntu-latest
    name: Check C Styling
    steps:
    - name: Checkout this commit
      uses: actions/checkout@v3
      with:
        fetch-depth: 2
    - name: uncrustify check
      uses: Daniel-Trevitz/uncrustify-check@v1
      with:
        configFile: 'uncrustify.cfg'
```
