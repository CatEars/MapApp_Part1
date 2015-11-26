# Part A - Introduction


#### tl;dr

![alt text](https://github.com/CatEars/MapApp_Part1/blob/master/product.png)


#### What are we going to do?

This is a project about creating a map application that can show the
shortest path from a --> b for users. The user will click two points
on the map and then click the button. This will update the map with
the shortest path between where the user clicked.

We will run the application through a webserver so we will learn a
little bit about hosting webpages and running a server. The project
will mostly be written in python but there will be some HTML, CSS and
JavaScript involved. If you are doing anything on the web you cannot
really avoid those three...

#### What are we going to ignore?

We are not going to try and make this webserver available on the
internet. This way we don't have to deal with any security
issues. Registering a domain and making your page show up on the
internet is also something that is not trivial to do.

#### What you are going to need

In order to do this project you need a linux machine running an OS
similar to ubuntu with python3 installed. You also need to know a
little bit about how to code in python and having experience with
HTML, CSS or JavaScript helps. If you know how to define functions,
loop using `for`, conditional statements using `if ... elif ... else`
you should be on a good foot. You will **not** need to know anything
about `class` or object orientation. I will also assume that you know
how to navigate the command line with commands such as `cd` and `ls`.

Some of the things in here can be done with a windows machine, or a
linux with, say, arch linux installed but the tutorial is written with
the above prerequisites in mind.

## Virtualenv

#### tl;dr

`sudo apt-get install python-virtualenv`

`virtualenv --python=/usr/bin/python3 venv`

The first command installs virtualenv on your computer and the second
one creates a virtualenv in the directory "venv" which will be located
in the same directory that you run the command. It will be installed
with python3.

#### What is a virtualenv?

Virtualenv is another installation of python. It just important enough
to be installed where your other programs are. The correct
technobabble is: "A virtualenv is a local distribution of python."

#### Why is a virtualenv usefull?

The advantages of storing a different installation of python like this
on your computer is that you can install different packages
(libraries) on different virtualenv. In this tutorial we will use
flask and pytest but if you later on will be making a homepage for
your pet you might want to use the fictional packages py_pet_server
and py_pet_test. Or perhaps (more likely) use django as a server.

## Installing libraries

#### tl;dr

`source venv/bin/activate`

Often when starting up a project I get very excited and want to start
coding immediately. However when starting from scratch like this we
need to install a lot of things before we get to the fun stuff ;). I
promise however that in the next part we will have a webserver up and
running!

We will be installing the libraries into the virtualenv. In order to
do this we need to **activate** the virtual env. We do this by typing
`source venv/bin/activate`. You should now see `(venv)` prepended to
your command line. This means that the virtualenv is activated. To
deactivate the virtualenv we would type `deactivate` and everything
would be back to normal. 

If we do not activate our virtualenv we will do stuff with the
system-wide installation of python and this will require us to install
things using `sudo`. All kudos to sudo but we want the libraries only
to exist in the virtualenv. When running the code we will also
**always** need to activate the virtualenv first. So make sure that
you look for the little `(venv)` before running anything ;)

### Flask

#### tl;dr

`pip install Flask==0.10`

#### What is flask?

flask is known to programmers as a micro web framework. Web framework
means that it is a code library that gives us helpful functions to
create something that does stuff with the web (it really is that
general, I'm not making this stuff up). The micro comes from the fact
that it tries to work with minimal effort from the programmers
side. Less is more =)

#### Why do we use flask?

The reason we use flask is because it is very simple. We can focus on
making something that works instead of making something super duper
professional. If we want to configure our webserver to do "all kinds
of stuff" flask is not necesarrily the best framework to use but for
our purposes it works great!

### Pytest

#### tl;dr

`pip install pytest==2.8.2`

#### What is pytest?

Pytest allows us to easily test our code. This will be important when
we create bigger and more badass functions.

#### Why do we want to use pytest?

In some parts of our code we want to make sure that the code we have
written does what we want it to do. We want to **validate our
assumptions**.  When we have established some basic functions we want
to make sure that they work as intended. If they do we can use them to
build new functions that does more advanced things and if these work
we can use them to build more advanced functions etc. etc. etc.

The hardest bugs in software occur because something did not go as
planned far from where code is being changed. By using testing to test
correctness of functions and validate our assumptions we can rest
assured what might have gone wrong when we have these super bugs.

#### What about unittest?

Some might know that there is a testing library that comes bundled
with python from the beginning. I am not a big fan of it. It comes
from languages like Java and Smalltalk and in those languages you have
different ideas of what "good code" looks like. The unittest module is
designed to look a lot like Java code but we are writing this project
in python. =)


### Testing that everything is installed

Here are some commands to run to make sure that everything is
installed correctly.

`python --version`

should print something like `Python 3.4.0` or perhaps `Python 3.5.2`

If it prints `python 2.7.6` or something similar you should make sure
that you have activated the virtualenv, if not you will have to remove
the virtualenv `rm -rf venv` and create a new virtualenv. Make sure
that you add `--python=/usr/bin/python3`

Next up: flask

`python -c 'import flask'`

This should just run withou any output. If you see an `ImportError`
flask is not properly installed.

Lastly, pytest:

`python -c 'import pytest'`

The same thing should happen here as with importing flask.


