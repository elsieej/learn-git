# learn-git

## Học về git log
git log --oneline
- return
- w
- spacebar
- q

## Học về git branch
- feature/login
git push -u origin HEAD
git branch -D
git fetch -p
git switch -c
git branch -a
git push origin --delete

## Học về git merge
- merge conflict:
git add .
git merge --continue --no-edit -> Không edit
git merge --continue --> edit
git pull origin handleB
git reset --hard <Hash ID>
git push -f

## Học về git rebase
git checkout feature/login
git rebase feature
A--B--C--D--E--------F -> (feature) ---G'----H' (feature/login)
         \
           \ -----G----H -> (feature/login)

git checkout master
git rebase feature/login

git checkout README.md
git restore README.md

git reset README.md
git restore --source=<Hash ID> <file name>

# Học về git reset
git reset <Hash ID> -> Changes
git reset --soft <Hash ID> --> Staged Changes
git reset --hard <Hash ID> --> Lost
git reset --merge <Hash ID> --> Safe for reset --hard

# Học về git revert
git revert --no-edit <Hash ID>
git revert -m <number> --no-edit <HashID>

# Học về git squash
git rebase -i HEAD~3
squash

# Học về git amend
git commit --amend

# Học về git stash
git stash list -p
git stash show stash@{0} -p
git stash apply stash@{0}
git stash drop stash@{0}
git stash clear
