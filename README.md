## github-action-docker-build

An extremely simple docker image auto build for your repository, made in order to replace in open source Docker Hub build integration, which has gone to the payed tier.

The resulting image is stored in ghcr.io, which is free for open source projects.


The `dockerfile` should exist in project root.

Also links a built image back to the repository via adding the according `LABEL` instruction to the dockerfile in process of a build.


Usage example (include it in a workflow file, e.g. `.github/workflows/build.yml`):

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
    - uses: btmc/github-action-docker-build@v1
```

Generates an image on any commit to main branch or any tag.
