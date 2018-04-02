# Tutorial Git/ GitHub

## Creating online repository
Go to GitHub and click on "New Repository"
This just creates an online storage space where we can edit, store and read files.
We still don't have an access to it on our computer.

## Create a local repository
Basically, just create a folder where we'll pull the online repository. So far this folder in completely independent of the online repository.

## Use Git commands on the local repository
Using the ```cd``` command into Terminal, go inside the folder created previously.
Then use: ```git init```. This tells the computer to recognise this repository (folder) as a local Git repository.

## Connect local repository to GitHub repository
On GitHub, get the HTTP link to the (online) GitHub repository.
In Terminal:
git remote add origin https://github.com/username/myproject.git
```remote``` is a descriptor of ```origin```: the origin is Not the computer but somewhere online.
The above command  tells Git there's a remote repository called ```my project```, and it's where we want our local repository changes to go.
To confirm and check that's right, type:
```git remote -v```
This gives a list of all the remote origins our local repository knows about.

## Create a file inside the local repository
In Terminal, ```touch Readme.txt``` or ```testFile.cpp``` or any file.

## See the current status of the repository 
Terminal: ```git status```
1) Tells us which branch we're located at.
2) Shows us "untracked" files, that is files that Git is ignoring for now.
3) Possibly other stuff not covered in this tutorial

## Add Commit Push
#### Add
To make Git notice that we added a new file in our repository, in Terminal:
```git add Readme.txt```
If we added multiple files, fastest way is:
```git add -A```

#### Commit
Commit command is to take a "snapshot" of the whole project at the current time.
In Terminal:
```git commit -m "message describing what is specific in this snapshot"```
Tips: Write the message in present tense. It describes what the commit does, and not what it did. We can always find back this particular snapshot at any time.

#### Push
To upload or "push" the changes to the GitHub remote repo:
1st time we push:
```git push -u origin master```
This is necessary because the computer needs to know from where it looks at to make changes. Here it will push the master branch to the online repo.
All the other times if we want to push from the master branch again:
```git push```
Push command updates definitively the GitHub repo.










