# Part A - Introduction


#### tl;dr

![alt text](https://github.com/CatEars/MapApp_Part1/blob/master/product.png)


#### What are we going to do?

This is a project about creating a map application that can show the
shortest path from a --> b for users. We will also run it through a
webserver so we will learn a little bit about hosting webpages and
running a server. The project will mostly be written in python but
there will be some HTML, CSS and JavaScript involved. If you are doing
anything on the web you cannot really avoid those three...

#### What are we going to ignore?

We are not going to try and make this webserver available on the
internet. This way we don't have to deal with any security
issues. Registering a domain and making your page show up on the
internet is also something that is not trivial to do.

## Virtualenv
#### tl;dr

`sudo apt-get install virtualenv`

`virtualenv --python=/usr/bin/python3`

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


## Installing everything

Often when starting up a project I get very excited and want to start
coding immediately. However when starting from scratch like this we
need to install a lot of things before we get to the fun stuff ;). I
promise however that in the next part we will have a webserver up and
running!

### Flask

#### tl;dr

`pip install Flask==0.10`

#### What is flask?

flask is known to programmers as a micro web framework. Web framework
means that it is a code library that gives us helpful functions to
create something that does stuff with the web. The micro comes from
the fact that it tries to work with minimal effort from the
programmers side ;)

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
