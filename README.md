# lessons-ssh

## ssh
- `cd ~/.ssh`
- `ssh-keygen -t ed25519 -C "email@example.com" -f "file_name"`
- `eval "$(ssh-agent -s)"`
- `ssh-add ~/.ssh/id_ed25519`

## config
```shell
#work account
Host github.com-work
     HostName github.com
     User git
     IdentityFile ~/.ssh/github-work
#personal account
Host github.com-personal
     HostName github.com
     User git
     IdentityFile ~/.ssh/github-personal
```
- `vi ./.git/config`
```shell
[remote "origin"]
    url = git@github.com-work:work/lessons-ssh.git
```

## test
- `ssh -T git@github.com-work`

# notes
- `ssh-add -D id_ed25519_taelfy_git`
# resources
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
- https://gist.github.com/rahularity/86da20fe3858e6b311de068201d279e3