.htaccess
=========

To prevent apache from serving any files in `.git/` put the following in your
`.htaccess`:

    RewriteEngine On
    RewriteRule "^(.*/)?\.git/" - [F,L]
