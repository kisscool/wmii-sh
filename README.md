wmii-SH
=======

This is a [`wmii`](http://wmii.suckless.org/) configuration file customized to add widgets with user event handling while still being as Bourne Shell and POSIX friendly as possible.


Why?
----

Short answer : because I can.

Long answer : I really like the concept of being able to control my Window Manager the way wmii allows me to do it. I really like its ability to be customized in a purely language-agnostic way. It is powerful, it is simple, it is the kind of well conceived interfaces that make me love UNIX so much. I could have used a language more suited for the job, like the excellent [`wmiirc project`](http://github.com/sunaku/wmiirc) did with ruby, but I liked the idea to keep the minimalistic and raw UNIXy feeling of a Bourne Shell script.

In fact I encourage you strongly to go check alternative solutions if you are purely interested in the end result : they bring more configuration possibilities on the table and they are generally more mature than this little pet project of mine. But if you like the concept of configuring wmii through pure shell, then you could find something of interest here.

How to use wmii-SH
------------------

### Installation

First of all, clone this repository on your desktop

	$ git clone http://github.com/kisscool/wmii-sh.git ~/.wmii

Then copy the wmiirc_local.example file and customize it according to your needs

	$ cd ~/.wmii
	$ cp wmiirc_local.example wmiirc_local
	$ vim wmiirc_local

Launch wmii and enjoy

### Upgrade

Juste upgrade the repository like you would do with a normal git project. The .gitignore file has been configured to avoid conflicts with your local configuration and with files auto-generated by wmii

	$ git pull

### Configuring Widgets

In order to add a widget in your wmii status bar, you need to enter the following line in wmiirc_local :

	add_widget $name $refresh_rate $position

with the following arguments :

* $name is the name of the widget (it is also the name of the function which defines it in wmiirc)
* $refresh_rate is the number of seconds between each refresh of the widget visual informations. 0 means no refresh.
* $position defines where the widget will be placed. The widget with the higher number will be at the absolute right of the screen.

For example, in order to add the "load" widget with a refresh rate of 30 seconds :

	add_widget load 30 10


List of Widgets
---------------

* load
* disk
* mem
* network
* power (linux only for now)
* temperature
* clock
* volume
* transilien (Paris transport system, in real time)
* weather


Bug tracking
------------

I am using [`Ditz`](http://ditz.rubyforge.org/) in order to track bugs and todo lists in the project. Just do :

	$ gem install ditz
	$ ditz todo

to check the state of open tickets.
