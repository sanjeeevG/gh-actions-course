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