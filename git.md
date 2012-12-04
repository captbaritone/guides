Git
===

Add an existing repo to db.classicalcode.com, and name the repo `foo`. First
add `conf/gitolite.conf` in the gitolite-admin repo. Push those changes.

    cd /path/to/repo
    git remote add newremote git@db.classicalcode.com:foo
    git push newremote 
