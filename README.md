# Publish artifact to Kentik Notary

This [GitHub Action][action] publishes an artifact to the Kentik
Notary. Appropriate AWS credentials should be injected as
environment variables.

## Inputs

| Name          | Description                     |
| ------------- | ------------------------------- |
| *name*        | artifact name                   |
| *version*     | artifact version                |
| *arch*        | artifact architecture           |
| *system*      | artifact operating system       |
| *artifact*    | path to artifact                |

## Usage

```yaml
uses: kentik/notarize@master
with:
  name: artifact
  version: 1.0.0
  arch: x86_64
  system: linux
  artifact: /github/workspace/<artifact>
env:
  AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
  AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
  AWS_REGION: ${{ secrets.AWS_REGION }}
```

[action]: https://github.com/features/actions
