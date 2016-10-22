<div align="center"><img src="https://cloud.githubusercontent.com/assets/630550/19619834/43c460dc-9835-11e6-8652-1c8fff91cf02.png" alt="GTM Logo" height="115" width="275"></div>
# <div align="center">Git Time Metrics</div>
### Seamless time tracking for all your Git projects

<pre>$ gtm report -today -author Schenk

7129f00 <b>Remove post processing of status</b>
Fri Sep 09 20:45:03 2016 -0500 <b>gtm-vim-plugin</b> Michael Schenk

       20m 40s  53% [m] plugin/gtm.vim
       18m  5s  46% [r] Terminal
           15s   1% [m] .gitignore
       39m  0s          <b>gtm-vim-plugin</b> </pre>

<pre>$ gtm report -format timeline-hours -last-week -author Schenk

             <b>00.01.02.03.04.05.06.07.08.09.10.11.12.01.02.03.04.05.06.07.08.09.10.11.</b>
             ------------------------------------------------------------------------
<b>Sat Oct 08</b> |                                                          ▃▃▃             |       <b>17m  0s</b>
             ------------------------------------------------------------------------
<b>Sun Oct 09</b> |                      ▁▁▁   █████████▃▃▃██████▂▂▂   ▂▂▂                   |    <b>5h 33m  0s</b>
             ------------------------------------------------------------------------
<b>Tue Oct 11</b> |                                                       ▂▂▂         ▂▂▂    |       <b>16m  0s</b>
             ------------------------------------------------------------------------
<b>Fri Oct 14</b> |                                     ▂▂▂                                  |       <b>13m  0s</b>
             ------------------------------------------------------------------------
<b>Sat Oct 15</b> |                            ███▇▇▇███▇▇▇███▁▁▁▇▇▇▂▂▂▁▁▁▃▃▃▆▆▆███▇▇▇       |    <b>8h 11m  0s</b>
             ------------------------------------------------------------------------
                                                                                          <b>14h 30m  0s</b> </pre>

GTM is automatic, seamless and lightweight.  There is no need to remember to start and stop timers.  It runs on occasion to capture activity triggered by your editor.  The time metrics are stored locally with the git repository as [Git notes](https://git-scm.com/docs/git-notes) and can be pushed to the remote repository. 

### <center>Plugins</center>

Simply install a plugin for your favorite editor and the GTM command line utility to start tracking your time now.

<p><img src="https://cloud.githubusercontent.com/assets/630550/17458557/72247454-5bda-11e6-84ce-03364b8ac832.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458560/72397408-5bda-11e6-909c-c2dd2dad3b52.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458562/7264e2be-5bda-11e6-8311-bbed672ffb8f.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458559/72302916-5bda-11e6-886e-2a41f423b06f.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458563/7264f06a-5bda-11e6-9fb6-d0469730c1cb.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458556/72030a62-5bda-11e6-89e4-6a3921034aed.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458564/727d43a4-5bda-11e6-8b3c-56d3fb7bf988.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458555/71e4352e-5bda-11e6-89d3-e8ff2c3a86e2.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458561/72417ac2-5bda-11e6-9769-04cffc64397e.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458591/82e06c98-5bdb-11e6-8ae0-c5b2bd2fe97f.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/17458558/72269342-5bda-11e6-8194-d9bf030bd037.png" width="64" height="64">
<img src="https://cloud.githubusercontent.com/assets/630550/19619987/f9f7523a-9838-11e6-99da-c3fda05ce0d6.png" width="64" height="64"></p>

# Getting Started

### Install the latest GTM release

**Mac OS X**

The simplest way to install is to use [Homebrew](http://brew.sh)
```
brew tap git-time-metric/gtm
brew install gtm
```

**Windows**

- Download and run the windows installer from [here](https://github.com/git-time-metric/gtm/releases/latest)

**Arch Linux**

The package available in Arch Linux User Repository: [https://aur.archlinux.org/packages/gtm/](https://aur.archlinux.org/packages/gtm/)

```
yaourt -S gtm
```

**Manually install for Linux, OSX or Windows**

- Download and install the executable from [here](https://github.com/git-time-metric/gtm/releases/latest)


### Install a plugin for your editor

- [Sublime 3](https://github.com/git-time-metric/gtm-sublime3-plugin)
- [Atom](https://github.com/git-time-metric/gtm-atom-plugin)
- [Vim](https://github.com/git-time-metric/gtm-vim-plugin)
- [IntelliJ IDEA, PyCharm, WebStorm, AppCode, RubyMine, PhpStorm, AndroidStudio ](https://github.com/git-time-metric/gtm-jetbrains-plugin)
- [VSCode](https://github.com/nexus-uw/vscode-gtm)
- [Terminal](https://github.com/git-time-metric/gtm-terminal-plugin)

### Initialize a project for time tracking

<pre>$ cd /my/project/dir
$ gtm init

Git Time Metric initialized for /my/project/dir

     post-commit: gtm commit --yes
  alias.fetchgtm: fetch origin refs/notes/gtm-data:refs/notes/gtm-data
   alias.pushgtm: push origin refs/notes/gtm-data
notes.rewriteref: refs/notes/gtm-data
        terminal: true
      .gitignore: /.gtm/
            tags: tag1, tag2 </pre>

### Edit some files in your project

Check your progress with `gtm status`.

<pre>$ gtm status

       20m 40s  53% [m] plugin/gtm.vim
       18m  5s  46% [r] Terminal
           15s   1% [m] .gitignore
       39m  0s          <b>gtm-vim-plugin</b> </pre> 

### Commit your work

When you are ready, commit your work like you usually do.  GTM will automatically save the time spent associated with your commit. To check the time of the last commit type `gtm report`.
<pre>$ gtm report

7129f00 <b>Remove post processing of status</b>
Fri Sep 09 20:45:03 2016 -0500 <b>gtm-vim-plugin</b> Michael Schenk

       20m 40s  53% [m] plugin/gtm.vim
       18m  5s  46% [r] Terminal
           15s   1% [m] .gitignore
       39m  0s          <b>gtm-vim-plugin</b> </pre> 

### Optionally save time in the remote Git repository

GTM provides [git aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases) to make this easy.  It defaults to origin for the remote repository.

Time data can be saved to the remote repository by pushing.
<pre>$ git pushgtm </pre>

Time data can be retrieved from the remote repository by fetching.
<pre>$ git fetchgtm </pre>

## Getting Help

For help from the command line type `gtm --help` and `gtm <subcommand> --help`.

For addtional help please consult the [Wiki](https://github.com/git-time-metric/gtm/wiki).

# Known Issues

- Currently `git stash` is not fully supported.  You can certainly use git stash but your time may be assigned to the wrong commit. We will be adding support for stashing in the near future.

# Contributing
[![Build Status](https://travis-ci.org/git-time-metric/gtm.svg?branch=develop)](https://travis-ci.org/git-time-metric/gtm) [![Build status](https://ci.appveyor.com/api/projects/status/gj6tvm8njgwj0hqi?svg=true)](https://ci.appveyor.com/project/mschenk42/gtm)

For more detail on how to write plugins, check out the [Wiki](https://github.com/git-time-metric/gtm/wiki).

# Support

To report a bug, please submit an issue on the [GitHub Page](https://github.com/git-time-metric/gtm/issues)

Consult the [Wiki](https://github.com/git-time-metric/gtm/wiki) for more information.
