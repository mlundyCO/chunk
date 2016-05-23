To setup new chunk (Debian):

ssh into machine using IP user 'root' and pw provided in email

    ssh root@IP

change the root password

    passwd

create a new user with sudo permissions

    adduser newuser
    adduser newuser sudo
    
edit `/etc/ssh/ssh_config`

    AllowUsers newuser

Log out of root and make sure the new user is able to SSH
Edit `/etc/ssh/ssh_config`

    PermitRootLogin no

Now you should not log in as root
Update

    sudo apt-get update

Install mosh, vim, git, zsh

    sudo apt-get install mosh git vim zsh

Make zsh default shell

    chsh

When prompted for new shell enter:

    /bin/zsh

Login using mosh

    mosh newsuser@IP

Pull vimrc and zshrc from github (see vim repo) 
