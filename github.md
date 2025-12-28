# Github

1: Local Branch is a few commits behind master, so to catch up the latest master: first go `master` branch, do `git pull origin master`, and then go to my `local branch,` and then `git merge master`, if there is conflict: 

then resolve conflicts in VS code: 

  go to VS code and solve the conflicts, then `git status`, fix conflicts and run `git commit`(or use "git merge --abort" to abort the merge), then `git status`, `git merge --continue`, then type `:wq` to write and quit, then `git push origin local branch`.

2: Another way: go to `master`, do `git pull` , and then `git checkout local branch`, then `git rebase master` then fix conflicts, do `git log` to check commits and do `git diff master` to check , and then i do `git push origin local branch —-force-with-lease`
`gp -f origin feature/tradies-sign-up/add-feature-flag`

`git rebase —onto newparent oldparent`    replace the newparent to oldparent

3:`shift + z z` to come out of vim 

```ruby
git fetch upstream
git reset --hard upstream/master
git cherry-pick <hash 1>
git cherry-pick <hash 2>
// cherry-pick all of your commits then:
git push -f origin your-branch
```

4 git cleanup local branches

```ruby
git fetch -p && for branch in $(git branch -vv | grep ': gone]' | awk '{print $1}'); do git branch -D $branch; done
```

5 push to staging

change to staging, and pull, and then `git merge branch-name`

6 get the latest branch info `git pull origin branch-name`

7 sometimes u want to reset branch `git reset —-hard origin` 

8: `git branch -D <branch_name>`

9: how to push to staging: go to staging, `git pull`, if it is conflicted, do `git reset —hard origin/staging`,

then do `git pull`; `git merge your branch`

or you could delete your local staging and you go to master, `git branch -D staging` and then gco staging and you have a new branch, now `git merge your branch`

10: retrigger CI `git commit --allow-empty -m "Trigger CI”`
11: after rebase mater, do a force push without any commit changes
      `git push -f origin branch:branch`

1. amend last commit `gc!`
2. `git checkout .`to remove all the uncommitted changed file back
3. reset branch to be align with master: 

`git log --oneline
git reset --soft f3e4a663`

then you force push

1. change your branch name: `git branch -M newName` 
2. try to amend ur last commit, `git commit —amend`
3. `ctrl R` to search historical command
4. bundle config https://rubygems.pkg.github.com/rails username:token
5. `git fetch && git pull --rebase && git push`