# Scenario 1

I have a new empty remote repository in GitHub. In local, I have some code changes which I want to force commit from my local to the remote repository.

I have created a new repository in Git with a new branch named "In-progress". I have built a folder in my local file system where I have developed some code. I want to push the code from my local to the new repository in Git inside the "In-progress" branch. What Git commands should I use for this? Because if I clone the repository, I will be left with an empty repository. Instead, I want to push the existing code in my local file system directly to this new repository.

```sh
cd <your folder location>
git init
git remote add origin <URL of new repo>
git remote add origin https://github.com/divsinha99/KodeKloud-Engineer.git

# Switch to the branch where you want to push the changes (create branch if it doesn't exist):
git checkout -b In-progress

# Add all files to the staging area:
git add .

# Commit the changes
git commit -m "Initial commit"

# Force changes to GitHub with the local changes: 
git push -f origin In-progress

