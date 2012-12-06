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

Correct the last commit message:

    git commit --amend -m "New commit message"

Cone a specific branch of a repo:

    git clone user@git-server:project_name.git -b branch_name /some/folder
