# Chapter 2

## Git basics

If you can read only one chapter to get going with Git, this is it. This
chapter covers every basic command you need to do the vast majority of the
things you’ll eventually spend your time doing with Git. By the end of the
chapter, you should be able to configure and initialize a repository, begin and
stop tracking files, and stage and commit changes. We’ll also show you how to
set up Git to ignore certain files and file patterns, how to undo mistakes
quickly and easily, how to browse the history of your project and view changes
between commits, and how to push and pull from remote repositories.

## Getting a Git Repository

You can get a Git project using two main approaches. The first takes an existing project or directory and imports it into Git. The second clones an existing Git repository from another server.

### Initializing a Repository in an Existing Directory

If you’re starting to track an existing project in Git, you need to go to the
project’s directory and type

    $ git init

This creates a new subdirectory named `.git` that contains all of your
necessary repository files — a Git repository skeleton. At this point, nothing
in your project is tracked yet. (See Chapter 9 for more information about
exactly what files are contained in the `.git` directory you just created.)

If you want to start version-controlling existing files (as opposed to an empty
directory), you should probably begin tracking those files and do an initial
commit. You can accomplish that with a few `git add` commands that specify the
files you want to track, followed by a commit:

    $ git add *.c
    $ git add README
    $ git commit -m 'initial project version'

We’ll go over what these commands do in just a minute. At this point, you have
a Git repository with tracked files and an initial commit.
