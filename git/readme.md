# Git

1. [Add SSH key to your GitHub account](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account)

2. [Commit signature verification](https://help.github.com/en/articles/managing-commit-signature-verification) _(Optional)_

1. [Git Style Guide](https://github.com/agis/git-style-guide)

2. [Git Flow](https://danielkummer.github.io/git-flow-cheatsheet/) **(Recommended)**

3. [Git Flow by Atlassian](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

4. Configure `git up` command to use `rebase` and `autostash` when pull changes:

    ```
    git config --global alias.up "pull --rebase --autostash"
    ```

    If you'd rather this happened on every git pull, then you can do this:

    ```
    git config --global pull.rebase true
    git config --global rebase.autoStash true
    ```

    [Source](https://github.com/aanand/git-up)
