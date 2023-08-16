This repository holds the database and miscellaneous pipelines and ansible roles that can be used in various products at Samagra.

To setup these pipelines do the following. 

```
cd /home
git clone https://github.com/Samagra-Development/samagra-devops.git

# symbolic links to jenkins jobs folder
mkdir -p /var/lib/jenkins/jobs  # to ensure the base directory exists for sure
ln -s /home/samagra-devops/jobs/database /var/lib/jenkins/jobs/database
ln -s /home/samagra-devops/jobs/miscellaneous /var/lib/jenkins/jobs/miscellaneous

# Make sure we have right permissions set
cd /home/samagra-devops  # make sure you change the directory path if it's changed at cloning step
chown -R jenkins:jenkins jobs
chown -R jenkins:jenkins /var/lib/jenkins

systemctl restart jenkins

```
You configure the `inventory/hosts` file in ansilble_roles for your server

# Docs link
https://samagra-development.github.io/Samagra-DevOps-Guide/
