### An Instruction to Connect Your PC to Your Github Account


* ##### Install git on Your Computer

* ##### Config git on Your PC
    ```
    git config --global user.name "Your_Username_for_GitHub"
    ```
    ```
    git config --global user.email "Your_email@something.com"
    ```

* ##### Make an ssh-key
    ```
    ssh-keygen -t ed25519 -C "Your_email@something.com"
    ```

* ##### Add ssk-key into Your PC
    ```
    eval "$(ssh-agent -s)"
    ```
    ```
    ssh-add ~/.ssh/id_ed25519
    ```

* ##### Add the Code to Your GitHub Account
    ```
    cat ~/.ssh/id_ed25519.pub | clip
    ```
    > yourgithub -> settings -> ssh -> new-ssh-key

* ##### Make Sure the ssh is Connected
    ```
    ssh -T git@github.com
    ```

* ##### Create a Repository
    > yourgithub -> repositories -> New -> name -> Create repository

* ##### Clone the Repository on Your PC
    > your-repository -> code -> copy ssh-url
    ```
    git clone "The_repository_ssh_code"
    ```