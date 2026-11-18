If you have an existing SSH key, you can use the key to authenticate Git operations over SSH.

Checking for existing SSH keys
Before you generate a new SSH key, you should check your local machine for existing keys.

Note

GitHub improved security by dropping older, insecure key types on March 15, 2022.

As of that date, DSA keys (ssh-dss) are no longer supported. You cannot add new DSA keys to your personal account on GitHub.

RSA keys (ssh-rsa) with a valid_after before November 2, 2021 may continue to use any signature algorithm. RSA keys generated after that date must use a SHA-2 signature algorithm. Some older clients may need to be upgraded in order to use SHA-2 signatures.

Open Git Bash.(clic en simbolo window en barra inferior y en barra de busqueda escribe bash y clic en Git bash)

Enter ls -al ~/.ssh to see if existing SSH keys are present.

$ ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
Check the directory listing to see if you already have a public SSH key. By default, the filenames of supported public keys for GitHub are one of the following.

id_rsa.pub

id_ecdsa.pub

id_ed25519.pub

Tip

If you receive an error that ~/.ssh doesn't exist, you do not have an existing SSH key pair in the default location. You can create a new SSH key pair in the next step.

Either generate a new SSH key or upload an existing key.

If you don't have a supported public and private key pair, or don't wish to use any that are available, generate a new SSH key.

If you see an existing public and private key pair listed (for example, id_rsa.pub and id_rsa) that you would like to use to connect to GitHub, you can add the key to the ssh-agent.

For more information about generation of a new SSH key or addition of an existing key to the ssh-agent, see Generating a new SSH key and adding it to the ssh-agent.

# Generating a new SSH key and adding it to the ssh-agent
After you've checked for existing SSH keys, you can generate a new SSH key to use for authentication, then add it to the ssh-agent.

About SSH key passphrases
You can access and write data in repositories on GitHub using SSH (Secure Shell Protocol). When you connect via SSH, you authenticate using a private key file on your local machine. For more information, see About SSH.

When you generate an SSH key, you can add a passphrase to further secure the key. Whenever you use the key, you must enter the passphrase. If your key has a passphrase and you don't want to enter the passphrase every time you use the key, you can add your key to the SSH agent. The SSH agent manages your SSH keys and remembers your passphrase.

If you don't already have an SSH key, you must generate a new SSH key to use for authentication. If you're unsure whether you already have an SSH key, you can check for existing keys. For more information, see Checking for existing SSH keys.

If you want to use a hardware security key to authenticate to GitHub, you must generate a new SSH key for your hardware security key. You must connect your hardware security key to your computer when you authenticate with the key pair. For more information, see the OpenSSH 8.2 release notes.

Generating a new SSH key
You can generate a new SSH key on your local machine. After you generate the key, you can add the public key to your account on GitHub.com to enable authentication for Git operations over SSH.

Note

GitHub improved security by dropping older, insecure key types on March 15, 2022.

As of that date, DSA keys (ssh-dss) are no longer supported. You cannot add new DSA keys to your personal account on GitHub.

RSA keys (ssh-rsa) with a valid_after before November 2, 2021 may continue to use any signature algorithm. RSA keys generated after that date must use a SHA-2 signature algorithm. Some older clients may need to be upgraded in order to use SHA-2 signatures.

Open Git Bash.

Paste the text below, replacing the email used in the example with your GitHub email address.

ssh-keygen -t ed25519 -C "your_email@example.com"
Note

If you are using a legacy system that doesn't support the Ed25519 algorithm, use:

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This creates a new SSH key, using the provided email as a label.

> Generating public/private ALGORITHM key pair.
When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. Please note that if you created SSH keys previously, ssh-keygen may ask you to rewrite another key, in which case we recommend creating a custom-named SSH key. To do so, type the default file location and replace id_ALGORITHM with your custom key name.

> Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
At the prompt, type a secure passphrase. For more information, see Working with SSH key passphrases.

> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
Adding your SSH key to the ssh-agent
Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.

If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys.

In a new admin elevated PowerShell window, ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in Working with SSH key passphrases, or start it manually:

# start the ssh-agent in the background
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
In a terminal window without elevated permissions, add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.

ssh-add c:/Users/YOU/.ssh/id_ed25519
Add the SSH public key to your account on GitHub. For more information, see Adding a new SSH key to your GitHub account.

Troubleshooting SSH agent conflicts in Windows
In Windows environments, the native Windows OpenSSH implementation and the one included with Git for Windows (based on MSYS2/Bash) can coexist.

If you configure and save your passphrases in the Windows agent using PowerShell, Git may still prompt you for your passphrase during operations like git push. This can happen when Git for Windows uses its bundled ssh.exe (from MSYS2) instead of the Windows system OpenSSH client, and therefore can't talk to the Windows ssh-agent service.

To ensure Git uses the agent where you've stored your credentials, force Git to use the system's SSH binary by running:

git config --global core.sshCommand "C:/Windows/System32/OpenSSH/ssh.exe"
You may need to specify which ssh-keygen binary Git should use to avoid conflicts with the binary bundled with Git for Windows. To define which binary is used, run the following command:

git config --global gpg.ssh.program "C:/Windows/System32/OpenSSH/ssh-keygen.exe"
Alternatively, you can reinstall Git for Windows and select the Use external OpenSSH option during the installation process.