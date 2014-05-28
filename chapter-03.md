# Chapter 3

## Git Branching

Nearly every VCS has some form of branching support. Branching means you
diverge from the main line of development and continue to do work without
messing with that main line. In many VCS tools, this is a somewhat expensive
process, often requiring you to create a new copy of your source code
directory, which can take a long time for large projects.

Some people refer to the branching model in Git as its “killer feature” , and
it certainly sets Git apart in the VCS community. Why is it so special? The way
Git branches is incredibly lightweight, making branching operations nearly
instantaneous and switching back and forth between branches generally just as
fast. Unlike many other VCSs, Git encourages a workflow that branches and
merges often, even multiple times in a day. Understanding and mastering this
feature gives you a powerful and unique tool and can literally change the way
that you develop.

## What a Branch Is

To really understand the way Git does branching, we need to take a step back
and examine how Git stores its data. As you may remember from Chapter 1, Git
doesn’t store data as a series of changesets or deltas, but instead as a series
of snapshots.

When you commit in Git, Git stores a commit object that contains a pointer to
the snapshot of the content you staged, the author and message metadata, and
zero or more pointers to the commit or commits that were the direct parents of
this commit: zero parents for the first commit, one parent for a normal commit,
and multiple parents for a commit that results from a merge of two or more
branches.

To visualize this, let’s assume that you have a directory containing three
files, and you stage them all and commit. Staging the files checksums each one
(the SHA-1 hash we mentioned in Chapter 1), stores that version of the file in
the Git repository (Git refers to them as blobs), and adds that checksum to the
staging area:

    $ git add README test.rb LICENSE
    $ git commit -m 'initial commit of my project'

Running `git commit` checksums all project directories and stores them as
`tree` objects in the Git repository. Git then creates a `commit` object that
has the metadata and a pointer to the root project `tree` object so it can
re-create that snapshot when needed.
