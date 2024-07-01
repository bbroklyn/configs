# Useful Git Configurations

## Setting Global User Parameters

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

## Setting Up Automatic Credential Storage

##### To store credentials (e.g., GitHub Personal Access Token), use credential.helper store:

```bash
git config --global credential.helper store
```

## Generating an SSH Key

##### For connecting to GitHub via SSH, generate an SSH key:

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

## Adding SSH Key to GitHub

##### Copy and add your SSH key in GitHub settings:

```bash
cat ~/.ssh/id_rsa.pub  # Outputs your public key
```

## Changing Remote Repository URL to SSH

##### If you've cloned a repository using HTTPS, change it to SSH URL:

```bash
git remote set-url origin git@github.com:username/repository.git
```

## Checking SSH Connection to GitHub

```bash
ssh -T git@github.com
```
