#projet terraform

Configure the ssh git
ssh-keygen -t ed25519 -C "ton-email@example.com"
# start agent ssh git
$ eval $(ssh-agent -s)

$ ssh-add ~/.ssh/id_ed25519

$ ssh-add -l

$ ssh -T git@github.com
Hi labjebbane! You've successfully authenticated, but GitHub does not provide shell access.


#### troubleshooting conflit merge in GIT
git check-ignore -v main.tf variable.tf
git add main.tf variable.tf
git commit -m "Ajout des fichiers main.tf et variable.tf"
git rebase --continue
git commit -m "Ajout des fichiers main.tf et variable.tf"
git push origin main --force

git filter-branch --force --index-filter \
"git rm --cached --ignore-unmatch .terraform/providers/registry.terraform.io/hashicorp/aws/6.8.0/windows_amd64/terraform-provider-aws_v6.8.0_x5.exe" \
--prune-empty --tag-name-filter cat -- --all

git filter-branch --force --index-filter "git rm --cached --ignore-unmatch .terraform/providers/registry.terraform.io/hashicorp/aws/6.8.0/windows_amd64/terraform-provider-aws_v6.8.0_x5.exe" --prune-empty --tag-name-filter cat -- --all
git reflog expire --expire=now --all
git gc --prune=now --aggressive

#CMD GIT & TF

git status
git add .
git add main.tf
git commit -m "Mise à jour main.tf"
git push

terraform init
terraform plan
terraform validate
terraform apply
terraform destroy

git status
git add .
git commit -m "comment"
git push
git add main.tf main.yaml
git status
git remote -v -> show fetch and push
git push origin main
