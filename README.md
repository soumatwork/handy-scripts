Adding your SSH key to the ssh-agent

$ eval "$(ssh-agent -s)"
> Agent pid 59566

$ vim ~/.ssh/config

Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519

$ ssh-add -K ~/.ssh/id_ed25519  
