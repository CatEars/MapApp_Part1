# Part A - Introduction


#### tl;dr
This is what we are going to do:
[insert picture of finished product]

[What are we going to do? What will the finished product look like?]
[What are we going to ignore?]


## Virtualenv
#### tl;dr
`sudo apt-get install virtualenv`
`virtualenv --python=/usr/bin/python3`

[What is a virtualenv?]

Virtualenv is another installation of python. It just important enough
to be installed where your other programs are. The correct
technobabble is: "A virtualenv is a local distribution of python."

[Why is a virtualenv usefull?]

The advantages of storing a different installation of python like this
on your computer is that you can install different packages
(libraries) on different virtualenv. In this tutorial we will use
flask and pytest but if you later on will be making a homepage for
your pet you might want to use the fictional packages py_pet_server
and py_pet_test. Or perhaps (more likely) use django as a server.


## Installing everything


### Flask

#### tl;dr

`pip install Flask==0.10`

#### [What is flask?]

flask is known to programmers as a micro web framework. Web framework
means that it is a code library that gives us helpful functions to
create something that does stuff with the web. The micro comes from
the fact that it tries to work with minimal effort from the
programmers side ;)

#### [Why do we use flask?]

The reason we use flask is because it is very simple. We can focus on
making something that works instead of making something super duper
professional. If we want to configure our webserver to do "all kinds
of stuff" flask is not necesarrily the best framework to use but for
our purposes it works great!

### Pytest

#### tl;dr 

`pip install pytest==2.8.2`

#### [What is pytest?]

Pytest allows us to easily test our code

#### [Why do we want to use pytest?]

In some parts of our code we want to make sure that the code we have
written does what we want it to do. We want to *validate our
assumptions*.  When we have established some basic functions we want
to make sure that they work as intended. If they do we can use them to
build new functions that does more advanced things and if these work
we can use them to build more advanced functions etc. etc. etc.

The hardest bugs in software occur because something did not go as
planned far from where code is being changed. By using testing to test
correctness of functions and validate our assumptions we can rest
assured what might have gone wrong when we have these super bugs.


#### [Over unittest in stdlib?]

