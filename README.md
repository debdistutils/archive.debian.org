# Git LFS mirror of `archive.debian.org`

This git repository contains a mirror of
[archive.debian.org](https://archive.debian.org/), with external
objects stored using [Git LFS](https://git-lfs.com/).

This repository was created using rsync from [the mirrors of
archive.debian.org](https://www.debian.org/distrib/archive).  The
initial import came from `debian.snt.utwente.nl` on 2024-04-26, and
later synced with `rsync.archive.debian.org` on 2024-04-28.

## Cloning

The Git LFS objects are not available via GitLab, therefor to clone
this repository successfully you will need to disable Git LFS smudging
using the `GIT_LFS_SKIP_SMUDGE=1` environment variable like this:

```
GIT_LFS_SKIP_SMUDGE=1 git clone https://gitlab.com/debdistutils/archives/debian/archive.debian.org.git
```

Be careful about storage requirements: The git pack to download is
currently about 310MB and the unpacked checkout will be around 11GB.

# Signature Verification

Commits are signed using [my PGP
key](https://blog.josefsson.org/2019/03/21/openpgp-2019-key-transition-statement/)
with fingerprint:

```
pub   ed25519 2019-03-20 [SC]
      B1D2 BD13 75BE CB78 4CF4  F8C4 D73C F638 C53C 06BE
```

You may view git log and verify commit signatures them as follows:

```
git log --show-signature
```

To verify a single commit use something like this:

```
$ git verify-commit 5f2be2945d9ee15a0be74335018f4bebb2a2568f
gpg: Signature made Sat Apr 27 09:54:19 2024 CEST
gpg:                using EDDSA key A3CC9C870B9D310ABAD4CF2F51722B08FE4745A2
gpg: Good signature from "Simon Josefsson <simon@josefsson.org>" [ultimate]
$ 
```

## Contact

The maintainer is [Simon Josefsson](https://blog.josefsson.org/).
