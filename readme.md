# git hub action course
- Setting up and adding intial data
    - create repo & sync with visual studio code 
    - login to git hub  - it will give the instruction such as url, and device to code to authorize
        ```
        gh auth login 
        ```
    - initialize and rename master branch 
        ```
        git init
        code reademe.md
        code .gitignore
        git add . 
        git commit -m "first commit" 
        git branch -M main 
        git remote add origin https://github.com/sanjeeevG/gh-actions-course.git
        git push -u origin main
        ```
    - for editing the global config 
        ```
        git config --global --edit
        *** press i for intert and change value
        *** press esc +: wq for saving and to quit.

        - for adding user name and email 
            git config --global user.name "name"
            git config --global user.email "email"
        ```
    - generating ssh key
        - use gh cli command
        Ref: 
        https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows&tool=cli
        https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

        https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows&tool=cli

        ```
        ssh-keygen -t ed25519 -C "sanjeeev_sinha@hotmail.com"
        
        *** press enter to add/select default
        *** go to git bash terminal and list from ssh folder
            ls ~/.ssh
            pbcopy > ~\.ssh\id_ed25519.pub

        *** from powershell terminal 
            dir ~/.ssh
            Get-Content ~\.ssh\id_ed25519.pub | Set-Clipboard
            ssh-add ~\.ssh\id_ed25519
            
            ## in case you get error in adding to the ssh agent, do the following on powershell (in admin mode)

            Get-Service -Name ssh-agent | Set-Service -StartupType Manual
            Start-Service ssh-agent

        ```
# important tools
    - cron generator: https://crontab.cronhub.io/ 
    - Something has changed. 
    
