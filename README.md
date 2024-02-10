learning git form cloud champ's vid-

create a new repository in github, (where readme file wasn't added), then after that follow along the instruction in the blank repo. which were-
"
echo "# cloud-champ_learngit" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/cruellord/cloud-champ_learngit.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin https://github.com/cruellord/cloud-champ_learngit.git
git branch -M main
git push -u origin main

"
first make a seperate folder(mkdir) for the project.

where the first command creats a new README.md file and echos command to print in the empty file what is within the quotation, "# cloud-champ_learngit"

if we check "git status", it throws an error as git local repo hasn't been initialised.

then in the same local folder, initialize git repo, with the second commmand, now that folder has a local repo.

check using - git status, for the detection of readme file ready to be added, if it shows in red then it needs to be added 

to add, use "git add file_name.xyz" or "git add ." to add all files in the folder, now it is in stage.

recheck "git status" now, it should show added files in green font color as new file, file is now staged.

use "git commit -m "initial commit"" to commit and take a snapshot of staged file.

use "git branck" to check which branch is currently being used

if we try to push without setting an origin, "git push -u origin master", where push command to push to remote repo, -u to specify user details further, origin to specify standard username, and master to specify branch.

but it will fail as it is not connected to remote repo yet,to check press "git remote -v" is it show nothing then local repo isn't conncected to remote.

to conncet to remote repo, "git remote add origin [remote_repository)_url]"

rechecking if connected ot remote repo, "git remote -v" it returns urls to remote repo.

after adding the modified file to stage again and commiting again,retrying to push again, it is successful, git push -u origin master

---------------------

now making a second version and adding new file "app.py"

after writing new file in vscode's explorer pane, where all open editors and files and folders are listed, next to new untracted file there is a U symbol which suggest that file is untracted by git.

the steps to push - status> add> commit > push.

to commit directly by skipping the staging area,[git commit -a -m "new_commit"]
to commit without adding- git commit -am "commit_message"
(-am flag= automatic)

to create custom commands/alliases=
git config --global alias.ac "commit -am" == git commit -am == git ac "commit_message"

to correct the typo made in last commit's message =  git commit  --amend -m "correct_commit_message"


git stash save [save_name] , to stash and store it for later with a name

git stash list , to list all the saved stash name

git stash apply[list_index] , to pop the stash







------------

then we change the app.py to third version.

after modifing the file the U for untracked symbol changes to M for modified, 

status> add> commit > push.
----------------------

in the github page we see all commits in commits tab with commit message,on clicking each addition or modification we can see what changes have been made.

making a new branch, git branch [brach_name], this only creates a new branch, dosen't uses that branch automatically.

to shift branch, "git checkout [branch_name or commit_hash]

to make a new branch and shift to it,-
"git checkout -b [branch_name]

go to previously used branch, "git checkout -"

to delete a branch, "git branch -d "branch_name"
to list all local and remote branch, "git branch -a"
to list only remote branch, "git branch -r"


git origin add [url]

pull is a combination of fetch and merge

Get all the change history of the origin for this branch:git fetch origin

git merge origin/master- to merge current origin to master branch

Update the current branch from its origin using a single command:git pull origin

push current to default remote origin- git push origin

to rename origin remote to upstream: git remote rename origin upstream




then upon hitting "git branch" it gives all the existing branch name, ad a * infront of the currently used branch.

unless you push something form the newly created branch, it doesn't reflect the new branch name in the github



PULL REQUEST - it is a way to propose changes to a repo by submitting them for review and eventually merging into the main/master branch . it facilitates code review and ensures control in software dev workflow.

now to add the changes of different to the master branch, in github
, click "compare and pull requests" in the code tab, write the pull comment to be read by the master to request merging and review, then click "create pull request" and the changes are mentioned below,

then click on "merge pull request" and "confirm merge", or from command line using git merge 

now to clone into another device, "git clone [repository_url]
which asks for password if the remote repo is pvt.

git tags are human readable mutable commits for easier checkouts


BEST PRACTICE-
clean commit history-don't commit the whole code all at once, commit each funcionality, frequently, for better tracking

for better readablity of git log, git log --graph --oneline

to rename the master branch to custom name= git branch -M [name]



reverting- git reset --hard [commit_hash], deletes the leatest commits

git revert [commit_hash], makes a new commit by undoing the changes in the perticular commit.










# learning_git

to work with exiaasting project, we create a copy of the project in our own account(remote repo), by forking, click on fork and select your account

any folder that starts with your own account, it's name starts with origin

from where you have forked the project is called "upstream"
to add the upstream repo, "git remote add upstream [url]"


to make a copy of origin in local repo, clone it, "git clone [url]

