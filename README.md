#projet terraform

Configure the ssh git
ssh-keygen -t ed25519 -C "ton-email@example.com"
# start agent ssh git
$ eval $(ssh-agent -s)

$ ssh-add ~/.ssh/id_ed25519

$ ssh-add -l

$ ssh -T git@github.com
Hi labjebbane! You've successfully authenticated, but GitHub does not provide shell access.

