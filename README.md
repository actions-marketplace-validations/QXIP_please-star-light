# :star: Please Star First GitHub Action

### OSS Starring Partner

This GitHub Action automatically comments issues opened by non-stargazers.

## Usage Example

```yml
name: Starring Partner
on:
  issues:
    types: [opened, reopened]
jobs:
  # This workflow checks if a user has starred a repository and takes actions
  starcheck:
    runs-on: ubuntu-latest
    steps:
    - name: Please Star First
      uses: qxip/please-star-light@v4
      with:
        token: ${{ secrets.GITHUB_TOKEN }}
        message: "Please star this repository to motivate developers! :star:"
        # label: "stargazed"
        # autoclose: true
```
