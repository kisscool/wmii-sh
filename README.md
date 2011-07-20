Wmii-SH
=======

This is a [`Wmii`](http://wmii.suckless.org/) configuration file customized to add widgets with user event handling while still being as Bourne Shell and POSIX friendly as possible.

You can easily bypass my personnal configuration variables by writing yours in wmiirc_local

How to use Wmii-SH
------------------

First of all, clone this repository on your box :

	$ git clone http://github.com/kisscool/wmii-sh.git ~/.wmii

Then copy the wmiirc_local.example file and customize it to follow your needs and overwrite my personnal (bad) tastes

	$ cd ~/.wmii
	$ cp wmiirc_local.example wmiirc_local
	$ vim wmiirc_local

Launch Wmii and enjoy it

Bug tracking
------------

I am using [`Ditz`](http://ditz.rubyforge.org/) in order to track bugs and todo lists in the project.
