# About

drestic is restic with defaults

# Synopsis

```
install -D -m 755 <(curl https://raw.githubusercontent.com/mschmitt/drestic/main/drestic) ~/bin/drestic
install -D -m 644 <(curl https://raw.githubusercontent.com/mschmitt/drestic/main/restic.conf) ~/.config/restic.conf
install -D -m 600 /dev/null ~/.config/restic.password
openssl rand -hex 32 > ~/.config/restic.password
editor ~/.config/restic.conf
drestic init
drestic backup
drestic snapshots
drestic forget --prune
drestic mount ~/mnt
```

Optionally, alias _drestic_ to _restic_:

```
alias restic=~/bin/drestic # also add to ~/.bashrc
restic init
restic backup
restic snapshots
restic forget --prune
restic mount ~/mnt
```

# Suggestions for the user

- Backup the contents of _~/.config/restic.password_ independently.
- Replace _$RESTIC_PASSWORD_FILE_ with _$RESTIC_PASSWORD_COMMAND_ and read the password from a password manager.

# Example values for _$RESTIC_REPOSITORY_

- `/tmp/my-demo-backup`
- `/media/${LOGNAME}/Backup/restic-repo/`
- `sftp:backupserver:/export/foo/restic-repo/`

# Status

Experimental - Just playing with the idea of having a config file for restic.

# License

The author has released this software into the public domain.

https://creativecommons.org/publicdomain/zero/1.0/

**No Copyright**

The person who associated a work with this deed has dedicated the work to the public domain by waiving all of his or her rights to the work worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law. You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission. See Other Information below.

**Other Information**

In no way are the patent or trademark rights of any person affected by CC0, nor are the rights that other persons may have in the work or in how the work is used, such as publicity or privacy rights.  Unless expressly stated otherwise, the person who associated a work with this deed makes no warranties about the work, and disclaims liability for all uses of the work, to the fullest extent permitted by applicable law. When using or citing the work, you should not imply endorsement by the author or the affirmer.
