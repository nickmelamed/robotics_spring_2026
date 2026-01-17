# Solving Common (Git) Issues

It is inevitable that you are going to run into some issues with git. The goal of this file is to give you some starting points of what to try. Remember, you do **not** need to memorize all of this, and you can always look things up for further reference! 

## First Rule: Stop and Check State

Before doing **anything** when running into an issue on git, please be sure to run `git status` so you can see what is going on in terms of committed files, unstaged files, etc. You would be shocked at how many problems you can fix simply by running this command and going from there. 

## "I Staged the Wrong File!"

Sometimes, you might've run `git add` on files you didn't want to be staged yet. Say, for instance, you accidentally ran `git add secrets.txt`, so now your `git status` call looks like this: 

```bash 
Changes to be committed:
    modified: config.yaml
    modified: secrets.txt
```
To fix this, you can run `git restore --staged secrets.txt` to remove that file from the staging area. Your changes remain local, so nothing wrong with running this to avoid confusing commits! 

## "I Committed Something I Shouldn't Have!"

You can remove commits but keep your changes staged by running `git reset --soft HEAD~1`. 

If you want to also unstage those changes, run `git reset HEAD~1`. 

If you use `git reset --hard HEAD~1`, beware that you would be deleting the most recent commit on your current branch and **ALL** uncommitted changes in the staging and working directory. So try to avoid using this. 

Also, `HEAD` is referring to your current working position in the repository. It will typically point to your most recent commit.

## "I Need to Change my Last Commit!"

`git --amend` will allow you to change a commit message, add more files to the commit, etc. Only use this on your **own personal branches**. 

## "I Need to Unstage Files!"

`git restore --staged .` to unstage all files, `git restore -- staged FILE` to unstage a given file. 

## "I Need to Undo Changes to my Files!" 

If you've already committed the changes, run `git checkout HEAD -- path/to/file`. The `--` is telling you that you are specifying a file (not a commit or branch), and `checkout` is making sure that `HEAD` will include the most recent committed changes of that file. 

If the file hasn't been committed yet but is staged, you can run `git restore path/to/file` to get the same result. 

## "I Did Work on the Wrong Branch and now I Can't Find it! 

