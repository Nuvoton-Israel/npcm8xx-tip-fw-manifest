

Nuvoton Cerberus
=================

Getting the code
-----------------

To get the Cerberus source code, you need to have `repo` installed.  Details about `repo` can
be accessed from the project readme located at https://gerrit.googlesource.com/git-repo/+/refs/heads/master/README.md

Example `repo` installation:
```bash
mkdir ~/bin
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+rx ~/bin/repo
PATH=${PATH}:~/bin
```

Download the source using HTTP:
```bash
mkdir NuvotonCerberus
cd NuvotonCerberus
repo init -u ../ -b master
repo sync
```

Download the source using SSH:

Prerequisites:
- Your SSH key (`~/.ssh/id_ed25519`) must be added to your GitHub account (https://github.com/settings/ssh/new)
- `repo` tool installed (see above)

```bash
mkdir NuvotonCerberus
cd NuvotonCerberus
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
repo init -u ../ -m default-ssh.xml -b master
repo sync
```

To set your git identity for this repo, add `--config-name` to the `repo init` command (it will prompt for name/email).
If you have the manifest repo cloned locally, you can use the local path instead:
```bash
repo init -u /path/to/npcm8xx-tip-fw-manifest -m default-ssh.xml -b master
```

###Repo on Windows

The `repo` tool is designed to work in a Linux environment, so there are some difficulties working with `repo` in
Windows.  See the `repo` documentation for details regarding Windows support at https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/windows.md

If `repo` is still not working there are two other options for using `repo` in Windows.

1. Use Windows Subsystem for Linux (WSL).  This has the benefit of not needing anything special for repo to work, but
has the downside of not actually being a Windows development environment.

2. There exists an old version of `repo` ported to work in Windows.  Details of this project can be found on github at
https://github.com/esrlabs/git-repo.  See the README.md in that repo for installation details.

If no option for `repo` is working on Windows and Windows must be used, then git repositories must be manually cloned per
the `repo` manifest file.

