<!-- start title -->

# GitHub Action:Release Action

<!-- end title -->
<!-- start description -->

Releases an action in a consistent way to be used across action repos

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: atomicfi/action-composite-action-template@undefined
  with:
    # The github token used to push release tags
    github-token: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**           | **Description**                             | **Default** | **Required** |
| :------------------ | :------------------------------------------ | :---------: | :----------: |
| **`github-token`** | The github token used to push release tags  |             |   **true**   |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start examples -->

### Example usage

```yaml
name: Release
on:
  pull_request:
    types:
      - closed
    branches:
      - main
    paths:
      - action.yaml
jobs:
  release-action:
    steps:
      - name: Release action
        uses: atomicfi/action-release-action@v1
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}  

```

<!-- end examples -->