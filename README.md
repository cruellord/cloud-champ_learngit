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

retrying to push again, 








# learning_git

