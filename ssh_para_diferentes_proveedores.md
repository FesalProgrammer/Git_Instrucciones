Email: fesalprogramming@gmail.com
User ID: 38200327

CONFIGURING SSH KEYS FOR MULTIPLE GIT PROVIDERS
This guide provides detailed steps on how to configure SSH keys for various Git providers using GitBash on Windows.

Prerequisites
GitBash installed on your system.
Access to your Git provider accounts.
Step 1: Generate SSH Keys
Generate a unique SSH key for each Git provider to avoid conflicts and ensure secure authentication.

# For GitHub
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/id_ed25519_github -N ""

# For GitLab
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/id_ed25519_gitlab -N ""

# For autocode.git.epam.com
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/id_ed25519_autocode -N ""
Replace "your_email@example.com" with your actual email address.
Step 2: Start SSH-Agent and Add Keys
Start the ssh-agent

eval $(ssh-agent -s)
Add SSH keys

ssh-add ~/.ssh/id_ed25519_github
ssh-add ~/.ssh/id_ed25519_gitlab
ssh-add ~/.ssh/id_ed25519_autocode
Step 3: Create or Modify the SSH Config File
Configure your SSH client to use the appropriate key for each Git provider.

Open or create the SSH config file
nano ~/.ssh/config
Add configurations for each host
# GitHub configuration
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_github
  IdentitiesOnly yes

# GitLab configuration
Host gitlab.com
  HostName gitlab.com
  User git
  IdentityFile ~/.ssh/id_ed25519_gitlab
  IdentitiesOnly yes

# AutoCode EPAM configuration
Host autocode.git.epam.com
  HostName autocode.git.epam.com
  User git
  IdentityFile ~/.ssh/id_ed25519_autocode
  IdentitiesOnly yes
Once you have made your changes:
Press Ctrl + O (the Control key and the letter 'O' at the same time). This is the command to write the changes to the file.
After pressing Ctrl + O, nano will confirm the file name to write. It should display the name of the file you opened (/home/username/.ssh/config).
Press Enter to confirm the file name and save the changes.
Press Ctrl + X to exit nano. This command closes the editor.
Step 4: Add Public SSH Keys to Git Providers
For each Git provider, you need to add the corresponding public SSH key.

GitHub:

Copy the SSH Public Key > cat ~/.ssh/id_ed25519_github.pub | clip
Go to GitHub Settings → SSH and GPG keys → New SSH key.
Title your key and paste the contents of ~/.ssh/id_ed25519_github.pub
GitLab:

Copy the SSH Public Key > cat ~/.ssh/id_ed25519_gitlab.pub | clip
Go to GitLab Settings → SSH Keys -> Add new key.
Title your key and paste the contents of ~/.ssh/id_ed25519_gitlab.pub
AutoCodeEPAM:

Copy the SSH Public Key > cat ~/.ssh/id_ed25519_autocode.pub | clip
Go to GitLab Settings → SSH Keys -> Add new key.
Title your key and paste the contents of ~/.ssh/id_ed25519_autocode.pub
Step 5: Test SSH Connections
ssh -T git@github.com
ssh -T git@gitlab.com
ssh -T git@autocode.git.epam.com
You should receive a message confirming successful authentication. See example:

Welcome to GitLab, @your_email@example.com!
Any questions?
Do you have any questions, or would you like to book a demo?
Please contact us at: supportautocode@epam.com