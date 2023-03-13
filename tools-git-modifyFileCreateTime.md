## In the Mac OS system, every file has two main time attributes: "Create Time" and " Modify Time" they can be checked by clicking the file and selecting `get info` button.

## Changing those two attributes by using `setfile` command.
1. `setfile -d 'mm/dd/yy hh:mm:ss' filename` can change the create date.
2. `setfile -m 'mm/dd/yy hh:mm:ss' filename` can change the modified date.
Note: Install Xcode command line tools before using the setfile command in the terminal.

## In order to change the GitHub commitment time, try to use the below command.
`GIT_COMMITTER_DATE="Jul 14 09:22:12 2022" git commit --date="Jul 14 09:22:12" -am "js modified"`
、