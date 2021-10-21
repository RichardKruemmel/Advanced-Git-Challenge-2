# Advanced-Git-Challenge-2
Part 2
Amending
Complete the following steps:

[x] Create a new repo or use an existing one
[x] Create a new file db.secret with a secret message
[x] “Accidentally” commit your secret
[x] Take a screenshot of `git log -p`
[x] Fix your mistake: Add db.secret into your .gitignore, remove the secret file from the index (see hint below) and `git commit --amend` (if you want you can add --no-edit to skip the editor window for the commit message)
[x] Take another screenshot of `git log -p` and post both screenshots to slack

[x] Hint: To remove something only from the index use `git rm --cached db.secret` this leaves the file in your folder.

Cherry Picking + Amending

Add two more commits to your repo, so you have at least 3 commits
Your goal is to change the message of the commit that is 3 steps back (while leaving the two children alone)

Steps: 
write down the hash of the two latest commits somewhere: 
git log --oneline  (In the following we will refer to them as A, B, C where C is the most recent, they will appear as
C
B
A
)
git reset --hard <A>
git commit --amend
git cherry-pick <B> <C>
