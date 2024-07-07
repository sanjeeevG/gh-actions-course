## Github actions

# Reference
- https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#name


# Fundamental building blocks 
    - Workflows 
        - defined at repository level. ie. we have to create at repository 
        - define which trigger actually starts the workflow 
        - are composed on one or more jobs 
        - 
    - jobs
        - are defined at workflow level 
        - defines in which execution envirornment it can run 
        - it is composed of one or more steps 
        - jobs are run in parallel by default
        - 
    - steps 
        - defined at the job level 
        - define the actual scripts or actions it will run
        - steps run sequencially by default
    
    ```
        name: my workflow
        on: push 
        jobs: 
            my-first-job:
                runs-on: ubuntu-latest  #uses linux runners
                steps:
                    - run: echo "hello world as first job"
            my-second-job: 
                runs-on: ubuntu-latest
                steps:
                    - run: echo "hello world as 2nd job"
    ```

# Excercise
    - tools used: VS code.
        - *** make sure you have gihub action extention installed.
    - Create .github/workflow folder
    - create simple example as mentioned above or excercise 01-building-blocks-yaml

# Events that trigger workflows
    - Reference
    https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows
    - 

# workflow runners
    - Github hosted: standard and large
        - Managed by github (patching,security etc)
        - A fresh VM scoped to the Job, even dependent job will run on fresh VM
    - self hosted: custom config
        - user managed (security and patching is user responsibility)
        - Unclean VM can be scoped

