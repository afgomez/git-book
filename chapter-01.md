# Chapter 1

## Getting Started

This chapter will be about getting started with Git. We will begin at the
beginning by explaining some background on version control tools, then move on
to how to get Git running on your system and finally how to get it setup to
start working with. At the end of this chapter you should understand why Git is
around, why you should use it and you should be all setup to do so.

## About Version Control

¿What is version control, and why should you care? Version control is a system
that records changes to a file or set of files over time so that you can recall
specific versions later. Even though the examples in this book show software
source code as the files under version control, in reality any type of file on
a computer can be placed under version control.

-- Missing paragraph: explain how VCS changed my life or something. --

If you are a graphic or web designer and want to keep every version of an image
or layout (which you certainly would), it is very wise to use a Version Control
System (VCS). A VCS allows you to: revert files back to a previous state,
revert the entire project back to a previous state, review changes made over
time, see who last modified something that might be causing a problem, who
introduced an issue and when, and more. Using a VCS also means that if you
screw things up or lose files, you can generally recover easily. In addition,
you get all this for very little overhead.

### Local Version Control Systems

Many people’s version-control method of choice is to copy files into another
directory (perhaps a time-stamped directory, if they’re clever). This approach
is very common because it is so simple, but it is also incredibly error prone.
It is easy to forget which directory you’re in and accidentally write to the
wrong file or copy over files you don’t mean to.

To deal with this issue, programmers long ago developed local VCSs that had a
simple database that kept all the changes to files under revision control.
