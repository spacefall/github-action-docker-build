## github-action-docker-build

An extremely simple docker image build for your repository, built in order to replace in open source the docker hub integration, which has gone to the payed tier.

Usage example:

```
on:
  push:
    branches:
      - main
    tags:
      - '*'

jobs:
  build:
    runs-on: ubuntu-20.04

    steps:
    - uses: btmc/github-action-docker-build@main
```

Generates an image on any commit to main branch or any tag.
