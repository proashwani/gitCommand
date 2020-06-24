git version
git config --global user.name ""
git config --global user.email ""
git config --global --list
git config --list := showing all default properties
git config --global color.ui true := set the values  globally


git clone https://git.bureauveritas.com/frontoffice/verigates.git





git remote show origin :- showing the remote location
git init project-name := create new project-name






git stash :- save the local changes temporarly
git pull :-

=======================git log=================
git log --all
git log -3 := last 3 commit
git log --author <name>
git log --committer <name>
git log --after 2.days.ago
git log --after "2014-02-01" --before "2014-02-02"
git log --oneline
git log --graph
git log --oneline --graph
git log --pretty=format:"Commit Hash: %H, Author: %aN, Date: %aD"
git log --stat :-= showing how many times files are added/modify in commit (use in multiple time commit)

git log --oneline --name-status --grep 0234215 := find the file of the mantis id
git show --pretty="" --no-commit-id --name-status [commitID] := showing the commit details


===================== comparing tool ============
https://www.scootersoftware.com/support.php?zz=kb_vcs


git config --global diff.tool bc
git config --global difftool.bc.trustExitCode true
git config --global difftool.bc.path "D:\Beyond Compare 4\BCompare.exe"

check the difference
git diff HEAD ./bvlink/pom.xml

git difftool f7806ab6 0bccd689
git difftool --dir-diff f7806ab6 0bccd689
(left/right  = remote/history) change

git config --global merge.tool bc
git config --global mergetool.bc.path "D:\Beyond Compare 4\BCompare.exe"

git mergetool f7806ab6 0bccd689


================branch ==============
git branch <branch-name> := create a new branch locally
git push -u <remote> <branch-name> :- push local branch to remote
git branch or git branch --list :- view branch
git branch -d <branch-name> := delete branch
git checkout <name-of-your-branch> := switch in branch and checking the updates
1. before checkout must stash/commit the changes
2. branch should exist on local
 
git checkout -b <name-of-your-branch> := create branch and switch into it


============ checkout / reset /revert ===========


git branch
git status
--- do some modification in 

git status
git checkout filename :- discard changes from working area
git checkout . :- discard All changes from working area

git add .
git commit 
git reset HEAD * :- Unstage all the files and come in working area
git status

 
if your commit not push then use the reset 
RESET :- always work on the local history not remote
remove latest commit
git reset HEAD~1 :- move the changes to working area
git reset --mixed HEAD~1 :-  default mixed move the changes to working area
git reset --soft HEAD~1 :- move the changes to staging area
git reset --hard Head~1 :- Move the changes to every where
git reset HEAD~3 :- reset the history latest last 3 commit 
1.  move the change from top and files send to working area
2. 



git revert commitID :- revert the changes from remote 
Internally It is revert the changes and commit the last changes in remote
============= merge /rebase ========================================
