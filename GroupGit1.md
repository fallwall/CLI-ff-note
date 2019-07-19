# Group Git

Once settled in your groups decide who will be the Git Czar
*********
### Git Czar does:

1. Make a project repo called `git-group-morning` (Git enterprise is okay, make it public and initialize a README)

1. Share the git repo link with your team in slack.

1. In Settings, under collaborators, add your team members.

### All members do:
1. **Clone** the repo to your local machine. **Do not fork.** `cd` into the `git-group-morning` directory.

1. Type `git branch -a` to see which branch you are on, as well as, your remotes.

1. Create a branch as yourname-master `git checkout -b yourname-branch`. 
    > (i.e., git checkout -b maddy-branch)

1. Open the `README` in their text editor.

1. Write a variable with your first and last name on line 2.
    > `const name = 'Maddy Rombes'`

1. Check to see that changes were made using `git status`

**It should look something like this:**

```
On branch maddy-branch
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

7. `git add README.md` for staging and then `git commit -m "add readme"`. **Do Not Push yet.**

1. `git status` at this point will say nothing to commit.

1. Type `git push origin master`. **What is happening when we do this on the new branch we created?**

1. Now, let's push to the correct branch `git push origin yourname-branch`

### Git Czar does:
1. On Github, click on the branches button to see the branches from your team.

1. You should see all the branches from the other team members, make sure you have all the branches before moving on. 

### All members do:
- On Github, under the Your Branches section, make a pull request using the new pull request button, base should be set to head and compare will be the yourname branch. 

*OR*

- In the pull request tab, select New Pull Request, and then select base to be master and compare will be the yourname branch. Once confirmed click on Create Pull Request, add a message and click on Merge pull request. Confirm the merge.

### Git Czar does:
1. Go to the pull request tab, select the pull request to work on, confirm the PR. There should be a merge conflict. Click the resolve conflict button.

1. You will see the conflicts page.

1. There are command line instructions and an interface, *we will show you*, we don't recommend doing it this way and stick to using the github UI.

**You should see something like this:**

```
# git-group-morning
<<<<<<< david-branch
const name = 'David Whitlatch'
=======
const name = 'Maddy Rombes';
>>>>>>> master
```

>To see the beginning of the merge conflict in your file, search the file for the conflict marker <<<<<<<. When you open the file in your text editor, you'll see the changes from the HEAD or base branch after the line <<<<<<< HEAD. Next, you'll see =======, which divides your changes from the changes in the other branch, followed by >>>>>>> BRANCH-NAME. source

- At this point, you should see one team members name in the `README` file, the name remaining should be whose pull request was pushed up last.

4. Merge all your pull requests into master.

1. Make your changes, click mark as resolved, and commit the merge and confirm the merge.

### Everyone does:
1. `git checkout master` —— switch to the master branch
1. `git pull origin master` ——— get the changes from the master 
1. `git checkout yourname-branch` ———— to switch your branch
1. `git merge master` ———- to merge master changes into your branch

- Now everyone should see the updated file in their text editor. 

- Confirm your changes are the same as on github enterprise.

1. Switch to master branch, `git checkout master`
1. Delete your remaining branches `git branch -d yourname-master` [-d or -D ?](https://koukia.ca/delete-a-local-and-a-remote-git-branch-61df0b10d323)

`git log --oneline --decorate --graph --all` to see the history of what we just did.
