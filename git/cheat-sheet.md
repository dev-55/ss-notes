# Cheat Sheet

## Config
	```
	git config --list
	git config user.name "Name"
	git config user.email "mail@mail.com"
	```

## Repo

- Clone to different folder name
	```
	git clone https://github.com/sferik/sign-in-with-twitter.git signin
	```
	
- Clone to current folder (without creating additional folder)
	```
	git clone https://github.com/sferik/sign-in-with-twitter.git .
	```
	(From https://stackoverflow.com/questions/8570636/change-name-of-folder-when-cloning-from-github)
	
- URL of remote
	```	
	git remote -v
	```
- Add a remote
	```
	git remote add origin https://github.com/user/repo.git
	```
	(From <https://help.github.com/en/github/using-git/adding-a-remote>)

- Change URL for remote repository
	```
	git remote set-url origin new.git.url/here
	```

&nbsp; 
## Branch
- Create new local branch based on current branch
	```
	git checkout -b "branchName"
	git push --set-upstream origin branchName
	```
- Create local version of remote branch
	```
	git checkout --track origin/the_remote_branch_name
	```
	(From <https://www.git-tower.com/learn/git/faq/checkout-remote-branch> )

- Delete a branch
	```
	Local	git branch -d the_local_branch
	Remote	git push origin --delete theRemoteBranch 
	```
	(From https://makandracards.com/makandra/621-git-delete-a-branch-local-or-remote)

&nbsp; 
## Commit
- WIP:
	https://bitsnbytes.blog/2018/11/26/using-a-work-in-progress-commit/
- Revert: 
	https://stackoverflow.com/questions/8728093/how-do-i-un-revert-a-reverted-git-commit


&nbsp; 
## Stash
	```
	git stash
	git stash list
	git stash pop
	git stash apply
	```

## Credentials

- Force GitHub Login Prompt
	```
	git config --local credential.helper ""
	```
	(From https://stackoverflow.com/questions/13103083/how-do-i-push-to-github-under-a-different-username)
