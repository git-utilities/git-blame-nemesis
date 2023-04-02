# Git Blame Nemesis
[heading__top]: #git-blame-nemesis "&#x2B06; Find and git blame all files modified by author"


Find and git blame all files modified by author

## [![Byte size of Git Blame Nemesis][badge__main__git_blame_nemesis__source_code]][git_blame_nemesis__main__source_code] [![Open Issues][badge__issues__git_blame_nemesis]][issues__git_blame_nemesis] [![Open Pull Requests][badge__pull_requests__git_blame_nemesis]][pull_requests__git_blame_nemesis] [![Latest commits][badge__commits__git_blame_nemesis__main]][commits__git_blame_nemesis__main] [![License][badge__license]][branch__current__license]


---


- [:arrow_up: Top of Document][heading__top]

- [:building_construction: Requirements][heading__requirements]
  - [Git Submodules][heading__git_submodules]
  - [Package manager applications][heading__package_manager_applications]

- [:zap: Quick Start][heading__quick_start]
  - [Clone][heading__clone]
  - [Install][heading__install]
  - [Print usage][heading__print_usage]

- [&#x1F9F0; Usage][heading__usage]

- [&#x1F5D2; Notes][heading__notes]

- [:chart_with_upwards_trend: Contributing][heading__contributing]
  - [:trident: Forking][heading__forking]
  - [:currency_exchange: Sponsor][heading__sponsor]


- [:card_index: Attribution][heading__attribution]

- [:balance_scale: Licensing][heading__license]


---



## Requirements
[heading__requirements]: #requirements "&#x1F3D7; Prerequisites and/or dependencies that this project needs to function properly"


> Prerequisites and/or dependencies that this project needs to function properly


---


### Git Submodules
[heading__git_submodules]: #git-submodules "This repository makes use of Git Submodules to track dependencies..."

This repository makes use of Git Submodules to track dependencies, to avoid
incomplete downloads clone with the `--recurse-submodules` option...


```Bash
git clone --recurse-submodules git@github.com:git-utilities/git-blame-nemesis.git
```


To update tracked Git Submodules issue the following commands...


```Bash
git pull

git submodule update --init --merge --recursive
```


To force upgrade of Git Submodules...


```Bash
git submodule update --init --merge --recursive --remote
```


> Note, forcing and update of Git Submodule tracked dependencies may cause
> instabilities and/or merge conflicts; if however everything operates as
> expected after an update please consider submitting a Pull Request.


---


### Package manager applications
[heading__package_manager_applications]: #package-manager-applications "Certain things be required for error-free installation of this project"


> Certain things be required for error-free installation of this project


- `help2man` → Conversion tool to create man files


**Arch**


```bash
sudo pacman -S help2man
```


**Debian**


```bash
sudo apt-get install help2man
```


______


## Quick Start
[heading__quick_start]: #quick-start "&#9889; Perhaps as easy as one, 2.0,..."


> Perhaps as easy as one, 2.0,...


---


### Clone
[heading__clone]: #clone "Download source code via Git"


> Download source code via Git


```bash
mkdir -vp ~/git/hub/git-utilities

cd ~/git/hub/git-utilities

git clone --recurse-submodules https://github.com/git-utilities/git-blame-nemesis
```


---


### Install
[heading__install]: #install "How to install from Git repository"


> How to install from Git repository


```bash
cd ~/git/hub/git-utilities/git-blame-nemesis

make config

vim .config-make

make install
```


---


### Print usage
[heading__print_usage]: #print-usage "How to get help for git-blame-nemesis"


> How to get help for git-blame-nemesis


```bash
man git-blame-nemesis

git-blame-nemesis --help
```


______




## Usage
[heading__usage]: #usage "&#x1F9F0; How to utilize this repository"


> How to utilize this repository


- Change current working directory to a Git repository


```bash
cd ~/git/tor/arti
```


- Iterate over files that an author has committed


```bash
git-blame-nemesis --author S0AndS0
```


- At each commit hash and file found a prompt will be displayed


```
[Enter] git blame 2333659a maint/add_warning.py
```


> Note inputs of `q` or `n` will terminate script, and keyboard shortcuts such
> as <kbd>Ctrl</kbd> `^` <kbd>c</kbd> _should_ also function to stop blaming


______


## Notes
[heading__notes]: #notes "&#x1F5D2; Additional things to keep in mind when developing"


> Additional things to keep in mind when developing


This repository may not be feature complete and/or fully functional, Pull
Requests that add features or fix bugs are certainly welcomed.



______


## Contributing
[heading__contributing]: #contributing "&#x1F4C8; Options for contributing to git-blame-nemesis and git-utilities"


> Options for contributing to git-blame-nemesis and git-utilities


---


### Forking
[heading__forking]: #forking "&#x1F531; Tips for forking git-blame-nemesis"


> Tips for forking git-blame-nemesis


Start making a [Fork][git_blame_nemesis__fork_it] of this repository to an
account that you have write permissions for.


- Add remote for fork URL. The URL syntax is _`git@github.com:<NAME>/<REPO>.git`_...


```Bash
cd ~/git/hub/git-utilities/git-blame-nemesis

git remote add fork git@github.com:<NAME>/git-blame-nemesis.git
```


- Commit your changes and push to your fork, eg. to fix an issue...


```Bash
cd ~/git/hub/git-utilities/git-blame-nemesis


git commit -F- <<'EOF'
:bug: Fixes #42 Issue


**Edits**


- `<SCRIPT-NAME>` script, fixes some bug reported in issue
EOF


git push fork main
```


> Note, the `-u` option may be used to set `fork` as the default remote, eg.
> _`git push -u fork main`_ however, this will also default the `fork` remote
> for pulling from too! Meaning that pulling updates from `origin` must be done
> explicitly, eg. _`git pull origin main`_


- Then on GitHub submit a Pull Request through the Web-UI, the URL syntax is
  _`https://github.com/<NAME>/<REPO>/pull/new/<BRANCH>`_


> Note; to decrease the chances of your Pull Request needing modifications
> before being accepted, please check the
> [dot-github](https://github.com/git-utilities/.github) repository for
> detailed contributing guidelines.


---


### Sponsor
[heading__sponsor]: #sponsor "&#x1F4B1; Methods for financially supporting git-utilities that maintains git-blame-nemesis"


> Methods for financially supporting git-utilities that maintains git-blame-nemesis


Thanks for even considering it!


Via Liberapay you may
<sub>[![sponsor__shields_io__liberapay]][sponsor__link__liberapay]</sub> on a
repeating basis.


Regardless of if you're able to financially support projects such as
git-blame-nemesis that git-utilities maintains, please consider sharing
projects that are useful with others, because one of the goals of maintaining
Open Source repositories is to provide value to the community.


______


## Attribution
[heading__attribution]: #attribution "&#x1F4C7; Resources that where helpful in building this project so far."


> Resources that where helpful in building this project so far.


- [GitHub -- `github-utilities/make-readme`](https://github.com/github-utilities/make-readme)
- [StackOverflow -- List all developers on a project in Git](https://stackoverflow.com/questions/9597410/list-all-developers-on-a-project-in-git)
- [StackOverflow -- Multi Level Bash Completion](https://stackoverflow.com/questions/5302650/multi-level-bash-completion)


______


## License
[heading__license]: #license "&#x2696; Legal side of Open Source"


> Legal side of Open Source


```
Find and git blame all files modified by author
Copyright (C) 2023 S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```


For further details review full length version of
[AGPL-3.0][branch__current__license] License.



[branch__current__license]:
  /LICENSE
  "&#x2696; Full length version of AGPL-3.0 License"

[badge__license]:
  https://img.shields.io/github/license/git-utilities/git-blame-nemesis

[badge__commits__git_blame_nemesis__main]:
  https://img.shields.io/github/last-commit/git-utilities/git-blame-nemesis/main.svg

[commits__git_blame_nemesis__main]:
  https://github.com/git-utilities/git-blame-nemesis/commits/main
  "&#x1F4DD; History of changes on this branch"


[git_blame_nemesis__community]:
  https://github.com/git-utilities/git-blame-nemesis/community
  "&#x1F331; Dedicated to functioning code"


[issues__git_blame_nemesis]:
  https://github.com/git-utilities/git-blame-nemesis/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."

[git_blame_nemesis__fork_it]:
  https://github.com/git-utilities/git-blame-nemesis/fork
  "&#x1F531; Fork it!"

[pull_requests__git_blame_nemesis]:
  https://github.com/git-utilities/git-blame-nemesis/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"

[git_blame_nemesis__main__source_code]:
  https://github.com/git-utilities/git-blame-nemesis/
  "&#x2328; Project source!"

[badge__issues__git_blame_nemesis]:
  https://img.shields.io/github/issues/git-utilities/git-blame-nemesis.svg

[badge__pull_requests__git_blame_nemesis]:
  https://img.shields.io/github/issues-pr/git-utilities/git-blame-nemesis.svg

[badge__main__git_blame_nemesis__source_code]:
  https://img.shields.io/github/repo-size/git-utilities/git-blame-nemesis


[sponsor__shields_io__liberapay]:
  https://img.shields.io/static/v1?logo=liberapay&label=Sponsor&message=git-utilities

[sponsor__link__liberapay]:
  https://liberapay.com/git-utilities
  "&#x1F4B1; Sponsor developments and projects that git-utilities maintains via Liberapay"


<!--
  vim: wrap spell textwidth=79
-->
