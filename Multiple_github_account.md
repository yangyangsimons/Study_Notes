## Manage multiple github account in the same computer

Sometimes we may have two or more github accounts in order to mamnagement different contents, and we need to deal with those accounts in the same computer.

1. ### Delete the global config

```bash
git config --global --unset 'user.name'
git config --global --unset 'user.email'
```

2. ### Generate different SSH key for each account

For example, I got two different accounts named 'example1' and 'example2'. So I need to generate SSH key for those accounts respectively. Note, they must be given different names to avoid cover each other.

```bash
ssh-keygen -t rsa -C "example1@example.com"
```

this will generate two files in `~/.ssh` directory which are `id_rsa` and `id_rsa.pub`.

```bash
ssh-keygen -t rsa -f ~/.ssh/id_rsa_2 -C "example2@example.com"
```

this will generate two files in  `~/.ssh` directory which are `id_rsa_2` and `id_rsa_2.pub`.

3. ### Add the SSH key in github account, this can refer to another blog which can be found in my blogs

4. ### Modify the `config` file

use terminal to open the config file

```bash
open ~/.ssh/config
```

if this file not exist, create it before modify it.
if this file exist, then modify it as below(mainly `Host` and `IdentityFile`):

> \# example1  
Host github_example1  
HostName ssh.github.com  
User git  
IdentityFile ~/.ssh/id_rsa  
>
> \# example2  
Host github_example2  
HostName ssh.github.com  
User git  
IdentityFile ~/.ssh/id_rsa_2  

use the command below to confirm the modify is successful:

```bash
ssh -T git@github_example1
ssh -T git@github_example2
```

5. ### Set the local directory config

Get into the local directory using gitbash tool. 

```bash
git config user.name "github_example1"
git config user.email "example1@example.com"
```

6. ### Link the local directory with github directory 

```bash
git remote add origin git@github_example1:XXXX/example.git
```

use `git remote -v` confirm the link status

### End
