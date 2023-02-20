# uex-git
This repository has been created for practice during the class at the UEx.

# Basic commands

Add the new/modified/deleted files to the repo:
```
git add <filename>
```
Instead of `filename` you can use `.` or `--all` to add all the target files to the repository.

To delete a file from the repo:
```
git rm --cached <filename>
```
The `--cached` option removes the file from the staging area but remains intact inside the working directory.

To commit a change:
```
git commit -m "<comments>"
```

To push a commit from local to remote:
```
git push
```

Check the status of the repo:
```
git status
```

Reverts file changes:
```
git checkout -- <filename>
```

Move a file:
```
git mv <source> <destination>
```

Show commit logs:
```
git log
```
Common flags: `-p <num>` to limit the output, `--stat`, `-S <function_name>`, `--since`, `--pretty`.

Other options:
```
git reset, restore, revert
```

# Working with branches

Create a new branch and switch to it:
```
git branch <branch_name>
git checkout <branch_name>
```

Shorthand:
```
git checkout -b <branch_name>
```

Switch back to your master branch (**important**):
```
git checkout master
```

Basic merging (after commit changes) in the master:
```
git merge <branch_name>
```

Now that your work is merged in, you have no further need for the branch. You can delete the branch:
```
git branch -d <branch_name>
```

![basic-merging-2](https://user-images.githubusercontent.com/15891153/220135270-3fcb5c07-af16-4851-96fa-4b9fb8eadd33.png)

Credits to https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

# Solve merge conflicts

# Tagging

Like most VCSs, Git has the ability to tag specific points in a repository’s history as being important. Typically, people use this functionality to mark release points (v1.0, v2.0 and so on).

Listing the existing tags in Git is straightforward. Just type git tag (with optional -l or --list):
```
git tag
```

Creating tags:
```
git tag -a <number_of_version> -m "<tagging_message>"
```
where `number_of_version` can have the following format: v1.4, v1.8.5, etc.

Credits to https://git-scm.com/book/en/v2/Git-Basics-Tagging

# Issues and pull requests

Reference code in issues:
https://geeks.ms/jorge/2017/08/26/marcar-un-codigo-en-github-para-hacer-referencia-comentar-o-compartir/

Information on pull requests:
https://www.freecodecamp.org/espanol/news/como-hacer-tu-primer-pull-request-en-github/
