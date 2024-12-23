If we have write access to a users`/.ssh/` directory, we can place our public key in the user's ssh directory at `/home/<user>/.ssh/authorized_keys`.

1. Create new ssh-keypair with: `ssh-keygen`
2. Copy `key.pub` on the remote machine to `/home/<user>/.ssh/authorized_keys`
3. SSH login with private key: `ssh <user>@<ip> -i key`