# Generating a new SSH key

### Open Git Bash.
Paste the text below, substituting in your GitHub email address.

* full command :       ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

* Ssimple command :   ssh-keygen -t rsa 

This creates a new ssh key, using the provided email as a label.

> Generating public/private rsa key pair.

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]

At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".


> Enter passphrase (empty for no passphrase): [Type a passphrase]> Enter same passphrase again: [Type passphrase again]

> Add public key  to Github/Gitlab

$ clip < ~/.ssh/id_rsa.pub

### Copies the contents of the id_rsa.pub file to your clipboard

> Test  SSH 
* ssh -T  git@gitlab.com
Welcome to GitLab, @USERNAME !
