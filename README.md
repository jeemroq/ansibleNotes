# ansibleNotes
My personal ansible notes &amp; tricks

# Git cheat sheet

## Branch strategy
git clone your repository to get main/master on local.
then:
```
git branch <YourBranchName>
```
It creates your own branch on local.
```
git push -u origin <YourBranchName>
```
to synchronise your local branch to central.

Add your code...
Back to git, add your modification to be staged:
```
git add -A
```

validate
```
git commit -m "commit message"
```

synchronize to central
```
git push
```
on your central (gitlab/github) you can do a merge request.

GitLab propose to squash commits : if you had several previous commits, it will only save one commit for all the changes made on the branch.
You can also delete the branch when merging. Usefull if your branch is for specific task (fix, feature) and is no more relevant when code is merged.
When merge is done, you can go back to your local and synchronise back:
```
git checkout master
git pull
```
It will update the master branch (previously merged in central).
```
git fetch -p
git branch -d <YourBranchName>
```
It will synchronise the branch deletion from central and remove the local branch.

You are now able to go back to the first step for the next feature ;)