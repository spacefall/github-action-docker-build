## github-action-docker-build

An extremely simple docker image build for your repository, make in order to replace in open source Docker Hub integration, which has gone to the payed tier.

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

Also links a built image back to the repository via adding the according LABEL instruction to the dockerfile in process of a build.
