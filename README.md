# better-codecov-action

A replacement for the official [codecov.io](https://codecov.io/) GitHub Action with the following improvements:

 1. This action can be pinned (see [codecov/codecov-action#574](https://github.com/codecov/codecov-action/issues/574)).
 2. This action is much more lightweight because it does not ship its own Python interpreter (1MB vs 25MB).

# Usage

```yaml
- uses: mhils/better-codecov-action@add-commit-hash-here
  with:
    arguments: ''  # optional arguments for the official codecov uploader 
```
