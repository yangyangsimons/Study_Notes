# Install XAMPP in mac
When trying to install XAMPP in mac with a M1 chip. Apache server cann't start
solution are as follows:
1. check the port occupation.
`sudo lsof -i -n `
2. stop the build in Apache server in mac
`sudo apachectl stop`
3. restart XAMPP and run the Apache server, it will works