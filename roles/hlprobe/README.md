# HLprobe Deployment

## Variables to override

For now check ''defaults/main.yml'' for variables to override.

## Sudo as

The role depends on being able to sudo as hlprobe_username but does not use the ``sudo_as`` role in its list of meta dependencies. So you must use that role yourself in the playbook and specify your current username that you use to login over ssh with.

## HLprobe git access

To complete the first deployment you must run the role and it will halt at the git repo step because the hlprobe user is newly created and its keys not yet added to the hlprobe repos in gitolite. 

So transfer the keys manually and add them to the gitolite repos hlprobe and hlprobe-binaries before running your play again.