## Create SSH Key and Configure

### Create SSH Key Pair
# Generate a new SSH key pair using the Ed25519 algorithm:
ssh-keygen -t ed25519 -C "i use this key for git repositories"

# Press Enter to proceed. Specify the file location and filename, for example: /home/naseem91/.ssh/github_ed25519.
# Optionally, you can enter a passphrase for added security when prompted, or press Enter to skip.

### Add SSH Key to SSH-Agent
# Start the ssh-agent:
eval "$(ssh-agent -s)"

# Add your SSH private key to the ssh-agent (will be ask to add passphrase):
ssh-add ~/.ssh/id_rsa

