---
title: "How to set HomeBrew in an M1 Mac"
date: 2023-04-25T00:37:38Z
draft: false
categories: ["tools","webDevelopment"]
---
### What problems happens here?
When I installed brew following the instruction from the Homebrew official website, the error `zsh: command not found: brew` happens. 

### How to fix this problem?
I fixed this problem by editing the path, creating the missing .zshrc file, and exploring the path to this new file.
```
cd /opt/homebrew/bin/
PATH=$PATH:/opt/homebrew/bin
cd
touch .zshrc
echo export PATH=$PATH:/opt/homebrew/bin >> .zshrc
```