# Scenario 1:

I have a new empty remote repository in Github. In local, I have some code changes which I want to force commit from my local to remote repository. 

I have created a new repository in git with a new branch named as "In-progress". I have built a folder in my local file system where I have developed some code. I want to push the code from my local to the new repository in git inside "In-progress" branch. What git commands should I use for this, because if I clone the repository, I will be having an empty repository. Instead I want to push the existing code in my local file system directly to this new repository.


```sh
cd <your folder location>
git init
git remote add origin <URL of new repo>
git remote add origin https://github.com/divsinha99/KodeKloud-Engineer.git

# switch to the branch where you want to push the changes (create branch if not exists):
git checkout -b In-progress

# add all files to staging area:
git add .

# commit the changes
git commit -m "Initial commit"

# force changes to github with the local changes: 
git push -f origin In-progress
```
