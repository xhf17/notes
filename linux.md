# Notes for some command tools
## command
This note is based on [this blog](https://haydenjames.io/linux-securely-copy-files-using-scp/)
#### aliases
    `.bashrc`, `.bash_aliases`
#### scp

Copy file from a remote host to local host SCP example:

    `scp username@from_host:file.txt /local/directory/`

Copy file from local host to a remote host SCP example:

    `scp file.txt username@to_host:/remote/directory/`

Copy directory from a remote host to local host SCP example:

    `scp -r username@from_host:/remote/directory/  /local/directory/`

Copy directory from local host to a remote hos SCP example:

    `scp -r /local/directory/ username@to_host:/remote/directory/`

Copy file from remote host to remote host SCP example:

    `scp username@from_host:/remote/directory/file.txt username@to_host:/remote/directory/`
