# kottans-frontend

## Repository dedicated to participation in [Kottans](https://github.com/kottans/frontend) frontend course :smiley_cat:.

### My progress :rocket:
 - **General**
   - [ ] Git Basics
   - [ ] Linux CLI and Networking
   - [ ] VCS (hello gitty), GitHub and Collaboration
 - **Front-End Basics** 
   - [ ] Intro to HTML & CSS
   - [ ] Responsive Web Design
   - [ ] HTML & CSS Practice
   - [ ] JavaScript Basics
   - [ ] Document Object Model - practice
 - **Advanced Topics**
   - [ ] Building a Tiny JS World (pre-OOP) - practice
   - [ ] Object oriented JS - practice
   - [ ] OOP exercise - practice
   - [ ] Offline Web Applications
   - [ ] Memory pair game — real project!
   - [ ] Website Performance Optimization
   - [ ] Friends App - real project!

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


# Git and GitHub

1. [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)

During this course i:

1. Realized that 'versions' is not only about highly specialized software such as git and version control to varying degree can be found 
in almost every program. 

2. Worked with versions of a document (called revisions) in google docs.

3. Repeated and clarified the basic concepts of git (working directory, index, repository areas and their workflow). Got acquainted with the contents of the hidden `.git` folder. Learned how to add files into `.gitignore` manually and with using special symbols.

4. Updated git version and checked config info.

5. Discovered new terminal commands:
   - `rmdir` to remove directory;
   - `ls -a` to list hidden files;
   - `mkdir -p parent/child` to create nested directories with single command.
   
6. Repeated and used such git commands as: 
   - `git init`;
   - `git clone`;
   - `git status` (inspecting working tree and stage areas);
   - `git log` and `git show` (inspecting commits);
   - `git rm --cached <filename>` (unstaging files);
   - `git diff` (difference between working directory and last commit). 

7. Installed and first used next packages for linting - [HTML linter](https://htmlhint.com/), [CSS linter](https://stylelint.io/), [JS linter](https://eslint.org/). While googling discovered command `npm init -y` for generating empty npm project.

8. Worked with git documentation to find neccessary command options.

9. Got acquainted with Less command line pager and it's commands for navigating through the history of commits:
   - `j` or `↓` scroll :arrow_down: by a line
   - `d` scroll :arrow_down: by a half-page
   - `f` scroll :arrow_down: by a page
   - `k` or `↑` scroll :arrow_up: by a line
   - `u` scroll :arrow_up: by a half-page
   - `b` scroll :arrow_up: by a page
  
10. Learned commands for commits investigation:
    - used `git log --oneline`, `git log --stat`, `git log --patch/-p` and `git log --stat -patch` flags to display all commits in certain form;
    - used `git log --oneline <SHA>`, `git log --stat <SHA>` and `git log -p <SHA>` to display commits from the point where specific commit placed;
    - used `git show <SHA>`, `git show --stat <SHA>`, `git show --stat --patch <SHA>` to get specific commit.

11. Realized that each commit should make a change to just **ONE** aspect of the project. **Single-unit change** principle.
    
    > Work on one change first, commit that, and then change the second one.

    > The best way that I've found to think about what should be in a commit is to think, "What if all changes introduced in this commit were erased?". If a commit were erased, it should only remove one thing.

12. Learned about commit naming:
    - :white_check_mark: make it *short*;
    - :white_check_mark: response *what* was done;
    - :x: don't tell *how* it was done;
    - :x: don't tell *why* it was done;
    - :x: don't use *and*.

    > The best way that I've found to come up with a commit message is to finish this phrase, "This commit will...". However, you finish that phrase, use that as your commit message.

13. Learned about entities used for organizing commits structure:
    | Entity | Description |
    | --- | --- |
    | tags  | static commit pointers  |
    | branches | dynamic commit pointers |
    | `HEAD` | dynamic branch pointer |

    Practiced in creating and deleting tags/branches and switching between branches. Practiced in linking tags and branches with specific commits. Practiced working with multiple feature branches. 
    
    Learned useful commands for work with branches: 
    - `git checkout -b <new-branch-name>` (create branch and switch to it);
    - `git checkout -b <new-branch-name> <existing-branch-name>` (create branch pointing on another branch's last commit and switch to it);
    - `git checkout -b <new-branch-name> <SHA>` (create branch pointing on specific commit and switch to it);
    - `git log --oneline/--patch/--stat --all --graph` (log commits for all branches using graph);

14. Executed fast-forward and regular merges using `git merge <other-branch>` command. If we merge 2 branches commits will be added to the one which under `HEAD` pointer (current branch). Branch we merge into === current branch.

    > When we merge, we're merging *some other branch* ***into the current (checked-out) branch***. 
   
    > :bangbang: We're not merging two branches into a new branch. We're not merging the current branch into the other branch.

    > Fast-forward merge – the branch being 'merged in' must be ahead of the current branch. Current branch's pointer will just be moved forward to point to the same commit as the other branch.
    
    > Regular merge - two divergent branches are combined, merge commit is created.
    
15. Forced and resolved merge conflict.

    > Git tracks lines in files. A merge conflict will happen when the exact same line(s) are changed in separate branches. 
   
Most of all in the course I liked presenting simple analogies to explain complex things.
