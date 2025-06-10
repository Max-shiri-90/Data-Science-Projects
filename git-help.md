1 - install git on your computer

2 - config git on your pc

```
git config --global user.name "Your_Username_for_GitHub"
```
```
git config --global user.email "Your_email@something.com"
```

3 - make an ssh key

```
ssh-keygen -t ed25519 -C "Your_email@something.com"
```

4 - add ssk-key into your pc

```
eval "$(ssh-agent -s)"
```
```
ssh-add ~/.ssh/id_ed25519
```

5 - add the code to your github account

```
cat ~/.ssh/id_ed25519.pub | clip
```
```
yourgithub -> settings -> ssh -> new-ssh-key
```

6 - make sure the ssh is connected

```
ssh -T git@github.com
```

7 - create a repository

> yourgithub -> repositories -> New -> name -> Create repository

8 - clone the repository on your pc

> your-repository -> code -> copy ssh-url
```
git clone "The_repository_ssh_code"
```