<ol>
    <li>install git on your computer</li>
    <li>config git on your pc</li>
        ```
        git config --global user.name "Your_Username_for_GitHub"
        ```
        ```
        git config --global user.email "Your_email@something.com"
        ```
    <li>make an ssh key</li>
        ```
        ssh-keygen -t ed25519 -C "Your_email@something.com"
        ```
    <li>add ssk-key into your pc</li>
        ```
        eval "$(ssh-agent -s)"
        ```
        ```
        ssh-add ~/.ssh/id_ed25519
        ```
    <li>add the code to your github account</li>
        ```
        cat ~/.ssh/id_ed25519.pub | clip
        ```
        > yourgithub -> settings -> ssh -> new-ssh-key
    <li>make sure the ssh is connected</li>
        ```
        ssh -T git@github.com
        ```
    <li>create a repository</li>
        > yourgithub -> repositories -> New -> name -> Create repository
    <li>Clone the repository on your pc</li>
        > your-repository -> code -> copy ssh-url
        ```
        git clone "The_repository_ssh_code"
        ```
</ol> 