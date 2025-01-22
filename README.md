
#  WARNING:   Cerberus core upgrade on Jan 22nd 2025!  IGPS older branches do not compile any more. need to revert the Cerberus core back to this commit:
#             95b9f2b1e22a378e08bf1cbe6120f14e182a1b00



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
repo init -u https://github.com/Nuvoton-Israel/npcm8xx-tip-fw-manifest.git -b master
repo sync
```

Download the source using SSH:
```bash
mkdir NuvotonCerberus
cd NuvotonCerberus
~/.local/bin/repo init --config-name tali.perry1@gmail.com -u git@github.com:Nuvoton-Israel/npcm8xx-tip-fw-manifest.git -m default-ssh.xml -b master  --config-name
~/.local/bin/repo sync

```

###Repo on Windows

The `repo` tool is designed to work in a Linux environment, so there are some difficulties working with `repo` in
Windows.  See the `repo` documentation for details regarding Windows support at https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/windows.md

If `repo` is still not working there are two other options for using `repo` in Windows.

1. Use Windows Subsystem for Linux (WSL).  This has the benefit of not needing anything special for repo to work, but
has the downside of not actually being a Windows development enviroment.

2. There exists an old version of `repo` ported to work in Windows.  Details of this project can be found on github at
https://github.com/esrlabs/git-repo.  See the README.md in that repo for installation details.

If no option for `repo` is working on Windows and Windows must be used, then git repositories must be manually cloned per
the `repo` manifest file.

