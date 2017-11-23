# git-branch
Adding git branch on the Bash command prompt

This tutorial shows how to add git branch in bash command prompt:
  note:You will be able to see current branch in bash while you are inside that folder.

Steps:

1. First download 'git-prompt.sh' or copy all contents 
2. Save it to a file and rename it as 'git-prompt.sh' and save it somewhere like '/home'
3. Open file '.bashrc' in home. (It is hidden, so you have to press 'ctrl+h' to show all files.
4. Make sure you have  permissions to that file, else give permissions by typing 'sudo chmod 777 path/.bashrc' in terminal
5. After giving permissions open '.bashrc' file in any editor and add these codes below 
    
    source /home/gaius/.git-prompt.sh
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\[\033[01;37m\]\u@\h:\[\033[01;33m\]\w\[\033[32m\]\$(parse_git_branch)\[\033[00m\]\[\033[01;37m\]\$"

6. Save the file and restart bash again, voila..... Open your git folder to see the change.




      
      

      
      
     
