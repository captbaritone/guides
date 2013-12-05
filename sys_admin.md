Sys Admin
=========

Create a user called captbaritone:

    useradd captbaritone

Create a new group `www`



Set a password for captbaritone:

    passwd captbaritone

Add user captbaritone to the group ftp:

    usermod -a -G ftp captbaritone

Push ssh key to remote server

    ssh-copy-id user@host

Cent OS
=======

Give user 'bob' sudo permission:

    visudo

Add the line:

    bob    ALL=(ALL)       ALL
