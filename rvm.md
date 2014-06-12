# RVM

## What *IS* RVM?
Well, according to the [RVM](http://rvm.io/) website, "RVM is a command-line tool which allows you to easily install, manage, and work with multiple ruby environments from interpreters to sets of gems."

Also, it stands for **R**uby En**V**ironment **M**anager. (Originially Ruby Version Monitor.)

## Okay, Got It. So ... What Does That Mean? 

On your first day of Ada, you installed many, many things. One of those things was RVM; another one of those things was Ruby. Specifically, the most recent stable *version* of Ruby. For the first cohort, that was Ruby 2.0.0. For you guys, it's probably some insanely advanced, space-age version. Ruby 17.1.3? Maybe! You can find out which Ruby you're using by using this command in terminal:

`ruby -v`

My computer tells me: ruby 2.1.1p76 (2014-02-24 revision 45161), so I'm using Ruby version 2.1.1p76. Whatever yours is, most if not all of the projects you work on will use that version of Ruby. So why do you need a command-line tool to manage multiple versions of rubies?

Well, perhaps the Ada instructors will decide to torture you guys and make you try to refactor some of the first cohort's old projects. If you have on your computer a version of Ruby that is not compatable with the version of Ruby we used in our projects, your computer will get a sad. Since Ada doesn't want your computer to be sad, they had you install RVM immediately, to streamline this process, allowing you to switch painlessly back and forth from one Ruby to another.

If you have RVM installed (WHICH YOU DO, YAY), if you cd into a directory that is utilizing a Ruby version that you do not have installed on your computer, it will immediately tell you. Which is great! It will also tell you exactly what to type into the command line to install the appropriate version, but most likely it will be something along the lines of:

`rvm install 2.0.0`

Then, to swap to that version of Ruby, you can type:

`rvm use 2.0.0`

Now if you type 

`ruby -v`

The computer should tell you you're using ruby-2.0.0-p451. (Or something similar. The p451 stands for the patch release.)

Now, if you want to go back to your system Ruby, that's easy! 

`rvm use system`

will revert you back to the system Ruby.

