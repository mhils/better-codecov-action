# better-codecov-action

A replacement for the official [codecov.io](https://codecov.io/) GitHub Action with the following improvements:

 1. This action does not pull in code from external sources and can be pinned (see [codecov/codecov-action#574](https://github.com/codecov/codecov-action/issues/574)).
 2. This action is much more lightweight because it does not ship its own Node interpreter (1MB vs 50MB).

# Usage

```yaml
- uses: mhils/better-codecov-action@add-commit-hash-here
  with:
    arguments: ''  # optional arguments for the official codecov uploader 
```

# Development

`codecov.js` is simply built from [codecov/uploader](https://github.com/codecov/uploader/) with the following command:

```shell
esbuild --minify --bundle --platform=node --target=node14 --outfile=codecov.js ../codecov-uploader/bin/codecov.ts
```
