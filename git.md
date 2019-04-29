# Notes for Git
## git
This note is based on [this blog](https://docs.google.com/document/d/1z9ST0IvxHQ3HXSAOmpcVbFU5zesMeTtAc9km6LAPJxk/edit#), and [this](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)
* `git status`, `git status -s`, `git add`, `git commit -m 'message'`
* `git diff`: To see what you’ve changed but not yet staged, with no other arguments
* `git diff --staged`: what have been staged but have not committed, This command compares staged changes to last commit
* `git rm file`: If you simply remove the file from your working directory, it shows up under the “Changes not staged for commit”. it stages the file’s removal, The next time you commit, the file will be gone and no longer tracked. If you modified the file or had already added it to the staging area, you must force the removal with the -f option.
* `git rm --cached file`: you may want to keep the file on your hard drive but not have Git track it anymore. This is particularly useful if you forgot to add something to your .gitignore file and accidentally staged it, like a large log file or a bunch of .a compiled files. To do this, use the --cached option.
* `git log --stat`: some abbreviated stats for each commit.
* `git commit -m 'initial commit'
* `git add forgotten_file'
* `git commit --amend`': You end up with a single commit — the second commit replaces the results of the first.
* `git reset HEAD file`: Unstaging a Staged File
* `git checkout -- file`: to discard changes in working directory.
Git remote
* `git remote -v`: 
  * koke git://github.com/koke/grit.git (fetch)
  * koke git://github.com/koke/grit.git (push)
  * origin git@github.com:mojombo/grit.git (fetch)
  * origin git@github.com:mojombo/grit.git (push)
  
