This tutorial will take you through the very basics of writing and running a python script. By the end you should be able to produce your first musical note using code.

As with any instrument a bit of setup is needed before we get started. If you haven't made a folder for all the tutorial files you can do that now:
		`mkdir pythonformusicians/`
Then go into that folder:
		`cd pythonformusicians/`
(hint: if you start typing something in terminal and hit TAB it will autocomplete for you.)

Now we can pick up the instrument and get the feel for it. If you run `touch myfirstnote.py` and then `ls` you will see a new file, that's where we're going to be putting our code.

## A Note on Text Editors.
From TextEdit to VSCode, Nano to Vim not all text editors were created equal and their fanbases are fiercely loyal. Take some time to try out a few and see which you like. Don't worry, most are free and they aren't nearly as involved as a DAW or any music software really so you won't get locked in.

## Back to the Music.
If you've decided on a text editor go ahead and open the `myfirstnote.py` file. In it, paste this code and save the file.

```python
# myfirstnote.py
from musicpy import *

myNote = note('C', 4)

play(myNote, wait=True)
```

Now head back to the terminal and run `python3 myfirstnote.py`.

## Your First Error.
What just happened! The code did not run. That's ok, I knew it wouldn't. It probably spat something back like this:
```python
Traceback (most recent call last):
  File "/Users/yourname/Code/pythonfiles/myfirstnote.py", line 1, in <module>
    from musicpy import *
ModuleNotFoundError: No module named 'musicpy'
```
Don't panic. While it might be frustrating when things don't go according to plan, these error messages are actually your best friends. The trick is understanding how to read them.

The first line `Traceback` announces a little map plotting the path taken to arrive at the error. The next line is the first point on that map - a file: `blah/blah/myfirstnote.py` and a line: `line 1` this tells us *where* the error is. The last line tells us *what* the error is. In our case we've got a  `ModuleNotFoundError` code and a bit of information `No module named 'musicpy'`. 

To solve this error then, we need to get a module called `musicpy` from somewhere. This can be achieved by typing into terminal `pip install musicpy` and hitting enter. Now if you run `python3 myfirstnote.py` you should here a lovely middle C.

## What Did We Just Do?
`pip` is a bit like an app store for Python, it allows us to import collections of python code which other people have put together. In this case we've imported a collection of python files called `musicpy` created by [Rainbow Dreamer](https://github.com/Rainbow-Dreamer/musicpy) . This means we don't have to write everything from scratch ourselves.

## Dissecting the Code.
The first line of the code `from musicpy import *` allows us to import the functions from the files of the package `musicpy`. A function is a bit of code that takes some inputs, performs a task and returns the output. That's a very vague definition but that's because functions can do anything from adding two numbers together to opening a functional browser window. 

Functions in python are anything with brackets after them. Can you spot them in our code? We've got `note()` and `play()`. The things in the brackets are called the parameters or inputs, and they are what the function performs it's specific job on. 

For example we passed the function `note()` the arguments `'C'` and `4`. These correspond to the note name - 'C' and the octave number - 4. This returns a `note object` which has properties corresponding to the arguments given to the function, e.g. a note name of 'C' and an octave number of 4. 

Rather than having this `note object` float around in the computational ether, we tie it down by giving it a name. In the full line `myNote = note('C', 4)` what we've done is store that `note object` in a position in memory with the name `myNote`. Later on, when we call `play(myNote, wait=True)` we reference this position in memory and pass the play function the note object as an input. 

Phew. Got all that? Don't worry, as we go along and you experiment with writing more code yourself the concepts will start to gel. For now pat yourself on the back, you successfully played your first note using Python!