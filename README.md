![](./images/markdown-styling/cat-banner-top.png)

# kottans-frontend

## Repository dedicated to participation in [Kottans frontend course](https://github.com/kottans/frontend).

![](./images/markdown-styling/cat-banner-bottom.png)

![](./images/markdown-styling/box-shadow-top.png)
### My progress :rocket:

 1. **General**
    - [ ] Git Basics
    - [ ] Linux CLI and Networking
    - [ ] VCS (hello gitty), GitHub and Collaboration
  
 2. **Front-End Basics**
  
    - [ ] Intro to HTML & CSS
    - [ ] Responsive Web Design
    - [ ] HTML & CSS Practice
    - [ ] JavaScript Basics
    - [ ] Document Object Model - practice
  
 3. **Advanced Topics**

    - [ ] Building a Tiny JS World (pre-OOP) - practice
    - [ ] Object oriented JS - practice
    - [ ] OOP exercise - practice
    - [ ] Offline Web Applications
    - [ ] Memory pair game — real project!
    - [ ] Website Performance Optimization
    - [ ] Friends App - real project!
  
![](./images/markdown-styling/box-shadow-bottom.png)

### Markdown basics

Text formatting and readability matter. It's up to you to choose a particular style, but remember to make it readable. Using markdown in your repo is a good idea.

### Material-specific Requirements

The course includes links to different learning materials - video courses, tutorials, articles etc. We suggest the following approach to those materials:

1. Reading: for each article you are required to read please post the answers to the following questions in your respective repo. Don't worry, your answers will not be graded. It's just a way to reflect on what you have learned.

   - _name (at least) one thing that was **new** to you_
   - _name (at least) one thing that **surprised** you_
   - _name (at least) one thing you intend to **use in the future**_
  
2. Online courses: finish all tasks, add your reflection about them into README.

3. Videos: same as for the reading; watch the video, answer three questions.

## General

### Git and GitHub

1. [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)

      [<img src="./images/markdown-styling/screenshot-image-link.png" height="30px">](./images/completion-screenshots/version-control-with-git.png)

      ![](./images/markdown-styling/alert.png)

   During this course i:

   - Used just learned commands while trying to add 'after-commit' changes to the last commit of this review.

   - Realized that 'versions' is not only about highly specialized software such as git and version control to varying degree can be found in almost every program.

   - Worked with versions of a document (called revisions) in google docs.
  
   - Repeated and clarified the basic concepts of git (working directory, index, repository areas and their workflow). Got acquainted with the contents of the hidden `.git` folder. Learned how to add files into `.gitignore` manually and with using special symbols.

   - Updated git version and checked config info.

   - Discovered new terminal commands:
     - `rmdir` to remove directory;
     - `ls -a` to list hidden files;
     - `mkdir -p parent/child` to create nested directories with single command.

   - Repeated and used such git commands as:
     - `git init`;
     - `git clone`;
     - `git status` (inspecting working tree and stage areas);
     - `git log` and `git show` (inspecting commits);
     - `git rm --cached <filename>` (unstaging files);
     - `git diff` (difference between working directory and last commit).

   - Installed and first used [HTML linter](https://htmlhint.com/), [CSS linter](https://stylelint.io/), [JS linter](https://eslint.org/). While googling discovered command `npm init -y` for generating empty npm project.

   - Worked with git documentation to find neccessary command options.
  
   - Got acquainted with Less command line pager and it's commands for navigating through the history of commits:
     - `j` or `↓` scroll :arrow_down: by a line;
     - `d` scroll :arrow_down: by a half-page;
     - `f` scroll :arrow_down: by a page;
     - `k` or `↑` scroll :arrow_up: by a line;
     - `u` scroll :arrow_up: by a half-page;
     - `b` scroll :arrow_up: by a page.
  
   - Learned commands for commits investigation:
     - used `git log --oneline`, `git log --stat`, `git log --patch/-p` and `git log --stat -patch` flags to display all commits in certain form;
     - used `git log --oneline <SHA>`, `git log --stat <SHA>` and `git log -p <SHA>` to display commits from the point where specific commit placed;
     - used `git show <SHA>`, `git show --stat <SHA>`, `git show --stat --patch <SHA>` to get specific commit.

   - Realized that each commit should make a change to just **ONE** aspect of the project. **Single-unit change** principle.

     > Work on one change first, commit that, and then change the second one.

     > The best way that I've found to think about what should be in a commit is to think, "What if all changes introduced in this commit were erased?". If a commit were erased, it should only remove one thing.

   - Learned about commit naming:
     - :white_check_mark: make it *short*;
     - :white_check_mark: response *what* was done;
     - :x: don't tell *how* it was done;
     - :x: don't tell *why* it was done;
     - :x: don't use *and*.

     > The best way that I've found to come up with a commit message is to finish this phrase, "This commit will...". However, you finish that phrase, use that as your commit message.

   - Learned about entities used for organizing commits structure:
    | Entity | Description |
    | --- | --- |
    | tags  | static commit pointers  |
    | branches | dynamic commit pointers |
    | `HEAD` | dynamic branch/commit pointer |

   - Practiced in creating and deleting tags/branches and switching between branches. Practiced in linking tags and branches with specific commits. Practiced working with multiple feature branches.

   - Learned useful commands for work with branches:
     - `git checkout -b <new-branch-name>` (create branch and switch to it);
     - `git checkout -b <new-branch-name> <existing-branch-name>` (create branch pointing on another  branch's last commit and switch to it);
     - `git checkout -b <new-branch-name> <SHA>` (create branch pointing on specific commit and  switch to it);
     - `git log --oneline/--patch/--stat --all --graph` (log commits for all branches using graph);
 
   - Executed fast-forward and regular merges using `git merge <other-branch>` command. If we merge 2 branches commits will be added to the one which under `HEAD` pointer (current branch). `Branch we merge into === current branch`.

     > When we merge, we're merging *some other branch* ***into the current (checked-out) branch***.

     > :bangbang: We're not merging two branches into a new branch. We're not merging the current branch into the other branch.

     > Fast-forward merge – the branch being 'merged in' must be ahead of the current branch. Current branch's pointer will just be moved forward to point to the same commit as the other branch.

     > Regular merge - two divergent branches are combined, merge commit is created.

   - Forced and resolved merge conflict.

     > Git tracks lines in files. A merge conflict will happen when the exact same line(s) are changed in separate branches.

 

   - Learned how to undo changes using commands:
     - **git amend** - replace last commit with new one (new one created by changing last commit's index):
       - `git commit --ammend -m='...'` (update recent commit message if index is empty since last   commit);
       - `git add <updated-file>` -> `git commit --amend -m='...'` (add changes made after commit to index -> update recent commit content and message);
       - `git add <updated-file>` -> `git commit --amend --no-edit` (add changes made after commit to index -> update recent commit content).

     - **git revert** - create new commit with removed last/specific commit's changes. If 'a' character is added in commit A, if Git reverts commit A, then Git will make a new commit where 'a' character is deleted.
       - `git revert <SHA> -m='...'` - create new commit with removed/reversed changes made within defined commit.
  
     - **git reset** :warning: - erase commit from memory by moving HEAD and current branch pointer to another commit. Erased commit's fate defined by `--mixed` (default), `--soft` and `--hard` options. It is better to create backup branch for using this command.
       - `git reset <commit-reference>` (move HEAD and current branch pointer to defined commit, place erased commit in working directory);
       - `git reset <commit-reference> --soft` (move HEAD and current branch pointer to defined commit, place erased commit in index);
       - `git reset <commit-reference> --hard` (move HEAD and current branch pointer to defined commit, place erased in trash area).

   - Learned that to reference commits we can use not only SHA/tags/branches/HEAD, but also relative path. All types of references can be integrated in commands where indicator of specific commit needed.
  
   Most of all in the course I liked presence of simple analogies  and visualizations of how git workflow works.
