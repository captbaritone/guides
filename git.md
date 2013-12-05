Git
===

Add an existing repo to db.classicalcode.com, and name the repo `foo`. First
add `foo` to `conf/gitolite.conf` in the gitolite-admin repo. Push those
changes.

    cd /path/to/repo
    git remote add origin git@db.classicalcode.com:foo
    git push origin master

Add an existing repo to github and name the repo `foo`. First create the repo
on github. Then:

    cd /path/to/repo
    git remote add origin git@github.com:foo
    git push origin master

Correct the last commit message and contents:

    git commit --amend -m "New commit message"

Clone a specific branch of a repo:

    git clone user@git-server:project_name.git -b branch_name /some/folder

Commit only part of a file. This will prompt you through each chunk. You can
select the part(s) you want with `y` (stage this chuck), `n` (don't stage this
part), `s` (split this hunk into smaller parts).

    git add -p filename.ext

See what content has been staged:

    git diff --staged

Unstage a staged file:

    git reset filename.ext

Push new branch to new remote server:

    git push -u origin branch-name

