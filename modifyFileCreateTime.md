## In the Mac OS system, every file have two main time attribute: "Create Time" and " Modify Time", they can be check by clicking the file and select `get info` button.

## Changing those two attributes by using `setfile` command.
1. `setfile -d 'mm/dd/yy hh:mm:ss' filename` can change the create date.
2. `setfile -m 'mm/dd/yy hh:mm:ss' filename` can change the modify date.

note: installing Xcode command line tools before using setfile command in terminal.