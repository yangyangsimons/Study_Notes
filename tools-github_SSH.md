# How to remove and create SSH key
### create SSH key
1. first step : check the local ssh
`cd ~/.ssh`
if there is a ssh key already exist, you will find files like: `id_rsa.pub` , `known_hosts` , `id_rsa` and so forth.
2. second step: create a new ssh key:
`ssh-keygen -t rsa -b 4096 -C "XXX@example.com"`
if you already have a ssh key it will prompt *Enter file in which to save the key `(/Users/lynnyang/.ssh/id_rsa)`* just input *y(yes)*.
In case you will forget the password, do not enter any password there.
3. copy the ssh key and add it in the github page of "SSH and GPG keys"
`cat cat id_rsa.pub`
then copy all the character into "SSH and GPG keys";
4. Done.