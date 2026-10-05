# lecture1

Learning git basics for the first time

1) Create a new repository
2) "git clone" command to clone github repo locally
3) "git status" command to check whether files are modified
4) "git diff" command to check what are the new changes
    - --staged is used to see what changes are made for files that are staged before commit is done
5) "git add" command to stage the files
6) "git commit" command to checkpoint the changes
7) "git push" command to push the edited files up to github
8) "git log" is used to monitor the history of commits
    - --oneline short hash that identifies each commit
9) .gitignore is used so that github ignore the untracked files listed inside
10) "git switch -c my-branch" is to create a new branch called my-branch
    - Note: Branch is created for developers to build on top of main without changing main code
10) "git branch" is used to check which branch you are on
11) "git switch xxx" is to switch to xxx branch
12) "git push -u origin new_branch_name" so that uplink can be establish to push via new_branch_name
13) "git branch -d my_new_branch is used to delete "my_new_branch" branch
14) "git pull" is used to pull new changes from repo to local machine

Learning Virtual Environment
1)  A virtual environment is a separate, isolated Python setup for a project.
2)  "echo $PATH"" is to find the path where the terminal look for executable program.
3)  "which python" allows us to see which python executable the terminal used.
4)  Do not develop projects with system python
    - /usr/bin/python3
5) "python3 -m venv foo" -> used to create a virtual environment "foo" in your directory
6) 