---
theme: ./theme.json
author: Nicolas Borboën (nicolas.borboen@epfl.ch) | EPFL Dojo |
# date: x MMM dd, YYYY
date: Jan 19, 2024
paging: Slide %d / %d
---

# EPFL Dojo

A presentation on **Git Extras**.

---

## What is Git Extras

- https://github.com/tj/git-extras
- TJ Holowaychuk ([@tjholowaychuk](https://x.com/tjholowaychuk))
- Initial commit Aug 4, 2010
- 1763 commits, ⭐ 16.5k stars, 1.2k forks
- 64+ Git commands

---

## Everything happens in your terminal

> Complex Git commands made easy

A set of bash files that accomplish complex Git effortless.

---

## Installation

You probably already know the drill:

- `[sudo] {apt,dnf,brew,pkg,yum} install git-extras`

https://github.com/tj/git-extras/blob/main/Installation.md

---

# Demo time `☃` <!-- https://www.youtube.com/watch?v=SwvCX94_EWI -->

```bash
echo "I came here to drink milk and kick ass. And I've just finished my milk." | cowsay -f milk
```

---

## 01 — How to get this? <!-- git summary -->

```git
project  : wp-dev
repo age : 6 years
active   : 406 days
commits  : 3075
files    : 33
authors  :
- 1058 LuluTchab                34.4%
- 419  ebreton                  13.6%
- 319  Dominique Quatravaux     10.4%
- 224  Laurent Boatto           7.3%
- 213  GregLeBarbar             6.9%
- 140  Hugo M. Muriel Arriaran  4.6%
```

---

### 01 — git summary `☃`

```bash
echo "$ Git summary for `pwd`"
git --no-pager summary
```

---

## 02 — Dr. Jekyll & Mr. Hyde! <!-- Sorry Luc-->

> 29 Luc Venries   0.9%
> 29 lvenries      0.9%

```git
git reauthor
```

---

## 03 — How to get this? <!-- git effort -->

```git
path                                          commits    active days

Makefile..................................... 193         98
README.md.................................... 109         56
.gitignore................................... 52          35
docker-compose.yml........................... 40          34
devscripts/copy-enac-from-prod.sh............ 14          7
devscripts/myip.............................. 6           5
devscripts/php-xdebug........................ 5           4
devscripts/local-restore-from-restic.sh...... 5           4
```

---

### 03 — git effort `☃`

```bash
echo "$ Git effort for `pwd`"
git --no-pager effort
```

---

## 04 — Where's the trunk? <!-- git brv -->

How to get a pretty listing of branches sorted by the date of their last commit?

---

### 04 — git brv `☃`

```bash
echo "$ Git brv for `pwd`"
git --no-pager brv
```

---

## 05 — Did someone give you a hand? <!-- git coauthor -->

Use git **coauthor**:

```git
commit b62ceae2685e6ece071f3c3754e9b77fd0a35c88 (HEAD -> master)
Author: user person <userperson@email.com>
Date:   Sat Aug 17 17:33:53 2019 -0500

    Add documentation files

    **Co-authored-by: user <user@email.com>**
```

---

## 06 — Branches, branches everywhere! <!-- git feature -->

Want to create a new feature branch? No problem:

```bash
$ git feature dependencies
Switched to a new branch 'feature/dependencies'
```

---

## 07 — Ignore all the things <!-- git ignoreio -->

Generate sample gitignore file from [gitignore.io](https://gitignore.io):

```sh
$ git ignore-io macOS

 # Created by https://www.toptal.com/developers/gitignore/api/macOS  
 # Edit at https://www.toptal.com/developers/gitignore?templates=macOS

 ### macOS ###
 # General

 .DS_Store  
 .AppleDouble
 .LSOverride
 [...]
```

---

## 08 — No clue about your current directory? `☃` <!-- git info -->

- Remote URLs:
- Remote Branches:
- Local Branches:
- Most Recent Commit:

`cat .git/config` ?

```bash
echo "Use git info!"
git info
```

---

## 09 — You can't blame gravity for falling in love. <!-- git guilt -->

git **blame**? git **guilt**!
> @todo: insert drake meme here.

```bash
# Find blame delta over the last three weeks
$ git guilt `git log --until="3 weeks ago" --format="%H" -n 1` HEAD
Paul Schreiber  +++++++++++++++++++++++++++++++++++(349)
spacewander     +++++++++++++++++++++++++++++++++++(113)
Mark Eissler    ++++++++++++++++
```

---

## 10 — AUTHORS.md? <!-- git authors -->

Populates the file matching `authors|contributors -i` with the authors of commits, according to the number of commits per author.

```bash
git authors
```

---

## 11 — CHANGELOG.md? <!-- git changelog -->

Generates a changelog from git(1) tags (annotated or lightweight) and commit messages.

```bash
git changelog
```

// See git-release

---

## 12 — MR or PR? MR is just better name all around. <!-- git pr -->

- Checks out a merge request from GitLab (`git mr`)
- Checks out a pull request from GitHub (`git pr`)

```bash
$ git mr 51
From gitlab.com:owner/repository
 * [new ref]         refs/merge-requests/51/head -> mr/51
Switched to branch 'mr/51'
```

---

## 13 — Hello Sherlock! <!-- git missing -->

Print out which commits are on one branch or the other but not both.
```bash
$ git missing master
< d14b8f0 only on current checked out branch
> 97ef387 only on master
```

---

## 14 — You can watch _obliterated_ on `Netflix`. <!-- git obliterate -->

Completely remove a file from the repository, including **past commits** and **tags**.

```bash
$ git obliterate secrets.json
```

---

## 15 — Wanna double check on GitHub? `☃` <!-- git browse -->

Opens the current Git repository website in your default web browser:

```bash
git browse
```

---

## 16 — https://whatthecommit.com/ <!-- git magic -->

Commits changes with a generated message:

```bash
git magic
```

> insert "it's magic gif here"

---

## Want more? Check out `git psykorebase`

https://github.com/tj/git-extras

---

# About

* This presentation uses https://github.com/maaslalani/slides.
* This presentation was given at a programming dojo at EPFL on 19 January 2024.
* Slides can be found here: https://github.com/ponsfrilus/prez-git-extras.

---

# End `☃`   

```bash
echo "Hope you liked it!" | cowsay -f hellokitty
```

[commands]: https://github.com/tj/git-extras/blob/main/Commands.md
