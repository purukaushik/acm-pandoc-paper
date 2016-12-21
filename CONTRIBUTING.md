#Contributing

You're welcome to find issues, file them and contribute to the repository with PRs. Please review [the open source code of conduct from OSI](https://opensource.org/codeofconduct).

### 1. Opening issues:
While submitting an issue please make sure you've tested it locally and make sure to include screenshots, scripts that you ran and a detailed description of what features you'd like to see in the repo.

### 2. Submitting PRs:

Please ensure the following:

1. First fork this repository and create your feature branch with a relevant branch name like `Issue#2_Fixing_Readme`.

2. After you finish fixing the issue, squash your commits down to one with:

   ```
   git rebase -i master
   ```

   Then in the commit message window, either `pick` or `reword` the first commit message and `squash` the rest:

   ```


   r e392483 Travis changes
   s a622df1 Travis changes
   s 0d11ccd Travis changes 2
   s 73b46bd Travis changes 2

   # Rebase 6992ef0..73b46bd onto 6992ef0 (4 command(s))
   #
   # Commands:
   # p, pick = use commit
   # r, reword = use commit, but edit the commit message
   # e, edit = use commit, but stop for amending
   # s, squash = use commit, but meld into previous commit
   # f, fixup = like "squash", but discard this commit's log message
   # x, exec = run command (the rest of the line) using shell
   # d, drop = remove commit
   ```

   A good article on squashing -> [https://ariejan.net/2011/07/05/git-squash-your-latests-commits-into-one/](https://ariejan.net/2011/07/05/git-squash-your-latests-commits-into-one/).

3. If you're committing a documentation change, like README.md, please add the `[ci skip]` string  in your message commits:

   ```shell
   git commit -m '[ci skip] - XXXXXXX'
   ```

   ​

4. When you're done submitting the PR, the travis-ci build for the PR would fail. But make sure your branch build works and be sure to mention this in the PR comments.

