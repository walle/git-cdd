git-cdd
=======

Simple proof of concept for workflow with git and Commit Driven Development. Inspiration from http://tosbourn.com/2012/08/development/commit-driven-development/

There are many things that could be improved, eg. naming, eror handling etc.
But this is just a quick hack to test things out. Written in like an hour, so I wouldn't be surprised if some things don't work.

How it works
------------

git-cdd is a simple shellscript that takes a commit message creates a branch from it, where you can do all changes related to the commit, then closes the branch and merges it with your previous branch.
This will only move the commit, no merge commits should be created.
The commit message will be the message you started the commit with.

Requirements
------------

Only tested on OS X, should work on any UNIX/Linux system that has a /tmp folder.

Installation
------------

To install the script, save the "bin" file (bin/git-cdd) somewhere and then make sure it's added to your path.

Usage
-----

The script acts as a git command. To use it invoke it like you would any other git command. eg.

```
  $ git cdd start "Implement awesome feature"
  ...make changes to implement feature...
  $ git cdd commit
```