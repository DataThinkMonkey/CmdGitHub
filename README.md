# CmdGitHub
My notes for how to use Github on the command line.

**Generate and ssh rsa key.**
ssh-keygen -t rsa

**Adding a new computer to connect with Github**
Add new ssh key to github
copy public key

 xclip -sel clip < ~/.ssh/id_rsa.pub

on github click on photo > settings
sidebar > SSH and GPG keys > new SSH key
paste in public key
click add ssh key

---

**Download repo**
git clone url
If already cloned, sync files:
git pull --rebase #sync with any changes from remote github
**Configure local cloned repo**
git config --global user.email "email address"
git config --global user.name "github username"
git config --global color.ui auto

**Edit or add files to directory on local machine**
git add file or dir
git commit -m "commit comment"
**If repo was cloned, you may need to remove origin.**
git remote remove origin
git push --set-upstream origin master
**Sets up local to remote ssh to github repo - only done once as part of set up**
git remote add origin git@github.com:username/repo.git
git remote -v #comfirm remote is set up
**Push to remote github**
git push -u origin master|branch name

**Branching Workflow**
_To create a branch and switch to it at the same time. -b branch, iss53 is the name of the branch_
git checkout -b iss53
**Add, commit and comment**
git commit -a -m 'comment'
**Switch back to master branch without merging**
git checkout master
**Can switch back to iss53 branch**
git checkout -b iss53
**To merge branch to master**
git checkout master
git merge iss53

**If conflicts use git status for troublehooting or mergetool**
git status
git mergetool
_then git status again to show conflict resolved._

**Remove directory**
git rm -r directories
git commit -m "commit comment"
git remote add origin
git push -u origin master

**Create local new repo**
git init

**Github GUI Clients**
GitKraken https://www.gitkraken.com/
- Linux, Mac, Windows
- Commerical license, Free for private use

SmartGit https://www.syntevo.com/smartgit/
- Linux, Mac, Windows

Git Desktop https://desktop.github.com/
- Windows, Mac

Git Cola https://git-cola.github.io/
- Written in python
- Linux, Mac, Windows

Eclipse Github plugin https://github.com/blog/1181-eclipse-git-plugin-2-0-released
Visual Studio Code integration

- https://www.theregister.co.uk/2015/12/07/visual_studio_code_git_integration/
- https://channel9.msdn.com/Series/Visual-Studio-Code-for-Mac-Developers/How-to-intergate-Visual-Studio-Code-and-GitHub

**Uses and Workflow for github** https://github.com/features

- Code Review https://github.com/features/code-review/
    - See every update
    - See Diffs, history and how it evolved over time.
    - Add comments, by line
    - request reviews and add user to request (they receive notifiation letting them know you need feedback)
- Project management https://github.com/features/project-management/
    - Create an issue to suggest a new idea or track a bug.
    - Create to-dos, checklists to coordinate and track parts of a project.
    - Assign others to an issue. They get notified.
    - Track milestones
- Team Management

- Social Coding
- Documentation
- Code Hosting
- Integrations https://github.com/marketplace
    - add plugins and apps to integrate with github
