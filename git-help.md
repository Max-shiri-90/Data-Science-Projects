### An Instruction to Connect Your PC to Your Github Account


* install git on your computer

* config git on your pc
    ```
    git config --global user.name "Your_Username_for_GitHub"
    ```
    ```
    git config --global user.email "Your_email@something.com"
    ```

* make an ssh key
    ```
    ssh-keygen -t ed25519 -C "Your_email@something.com"
    ```

* add ssk-key into your pc
    ```
    eval "$(ssh-agent -s)"
    ```
    ```
    ssh-add ~/.ssh/id_ed25519
    ```

* add the code to your github account
    ```
    cat ~/.ssh/id_ed25519.pub | clip
    ```
    > yourgithub -> settings -> ssh -> new-ssh-key

* make sure the ssh is connected
    ```
    ssh -T git@github.com
    ```

* create a repository
    > yourgithub -> repositories -> New -> name -> Create repository

* Clone the repository on your pc
    > your-repository -> code -> copy ssh-url
    ```
    git clone "The_repository_ssh_code"
    ```