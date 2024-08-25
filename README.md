# Repo Sync
Github action for creating Github mirrors from remote repositories.

## Example Usage

```yaml
name: Sync repository

on:
  schedule:
    - cron: '0 0 * * *'  # This will run at 00:00 UTC every day
  workflow_dispatch:  # This allows the workflow to be manually triggered

jobs:
  sync-repo:
    runs-on: ubuntu-latest

    steps:
    - name: Sync repository
      uses: reposyncer/reposync@v1.4
      with:
        name: gnu-nano
        url: https://git.savannah.gnu.org/git/nano.git
```
