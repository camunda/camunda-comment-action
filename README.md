## Setup

Add the following to you github repository `.github/workflows/main.yml` to enable the action:

```
on: 
  pull_request:
    types: [opened]

jobs:
  comment_job:
    runs-on: ubuntu-latest
    name: Label Pull requests
    steps:
      - name: Comment
        uses: camunda/camunda-comment-action@v1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

