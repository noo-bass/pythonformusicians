Installing python can actually be a massive ball-ache. Which is surprising given that it is used by so many people. But this is exactly the problem - there are about as many ways of installing python as there are people using it. 

This might make you apprehensive. This apprehension is normal. Don't worry. The most important thing to keep in mind throughout this book is that YOU ARE NOT GOING TO BREAK ANYTHING. 

There are a multitude of ways to destroy computers but the code we're going through in this book won't allow you to do that. If anything goes wrong it is easily undone.

## MacOS

I'm a Mac guy. If you aren't a Mac user I'll send you to another tutorial to get started. The result of most Windows tutorials just get you to a point where you are a Mac/Linux user anyway so go do that and come back. 

### The Terminal
If you've never written any code before welcome to terminal. Yes, that application that you've never opened is in fact your key to unlocking your computers true power. Go open it.

The vanilla terminal app on mac is fine but if you wan't to take things to the next level I can't recommend [iTerm2](https://iterm2.com/) enough.

When you open terminal for the first time you'll see something like:
			`yourcomputer:~ yourname$`
with a blinking cursor. This is where you are in the file structure of your computer. `~` (tilde) is shorthand for home it's the root file of your computer. It contains things you might be familiar with such as `Applications/`, `Desktop/`, `Downloads/` and `Documents/` . If you type `ls` (short for list) you'll see these familiar friends. 

Well done! You just wrote your first Bash command. I know you came here to learn about Python and we've already moved on to something else but you'll become good friends with Bash as we go along and it'll prove to be a powerful ally for almost everything you do with your computer.

### XCode-Select
`xcode-select --install` this can take a little time, agree to everything.

### Homebrew
Homebrew will be another powerful ally who will accompany you all the way through your Python journey. It's basically the app store for programming, only with fewer buttons and crappy iphone games. You can install [Homebrew](https://brew.sh/) here - just paste that first line into terminal and hit  enter. When it asks for a password it'll just be the password you use to logon to your mac (as long as the mac is yours - otherwise it'll be whoever's the admin is) - also note that you won't see any sign of input in the Terminal window, have faith, it's for your security.

Next we need to append Homebrew to our path. The path is a bit like a map, it tells Bash where it can find it's tools. 

Homebrew tells you what to do here, at the bottom of all the text it spat out but here it is if you cannot find it.
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
This puts Homebrew's location into the file `~/.zprofile` which is referenced by bash every time you open a new terminal window, so it knows where everything is.
### Downloading Python
Ok, finally we've got to a point where we can start thinking about downloading python.