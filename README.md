# How to change your python alias

I recently discovered a cool thing that will make your Python development a tiny bit more enjoyable. If you - like me - have different versions of python installed on your machine i.e. 2.7 and 3.6, you are most likely familir with typing something like this `$ python3 script.py` or maybe `pip3 install requests` in your terminal. And if you need to run a python2.x script you can simply use `python script.py` or `pip install requests`. 

The problem here is that i for the most time only use Python 3.x, and so i find it a little annoying that i have to type that `3` after `python` everytime. It is jsu extra work even though it seems like such a small thing i really wanted to fix this.

Luckily there is an easy solution to this. It turns out you can actually define your own aliases for various commands in the terminal. For instance, if you write in your terminal:

```sh

$ alias python=python3

```

and hit enter then you should be able to reference `python3` just by writing `python`. Amazing!

```sh

$ python --version
Python 3.6.1

```

But, this alias only lives as long as your terminal session lives. Meaning, that when you close your terminal and open it up again it has forgotten about your cool new alias. 

So, the way to fix this more permanently is to update your .bashrc file. The .bashrc file is a script that is executed whenever a new terminal session is started in. It is similar to the .bash_profile. You can look it up if your are more curous. What you have to do is the following:

```sh

cd ~/

```

Open up .bashrc file with nano or any editor
```sh

nano .bashrc

```

Paste in the following
```sh

alias python2=python2.7
alias pip2=pip2
alias python=python3
alias pip=pip3

```

To save and exit the file hit `CTRL + X` and hit `ENTER`.

The last thing to do is to run the script:

```sh

source ~/.bashrc

```

Now, you can test it in your terminal like this

```sh

$ python --version
Python 3.6.1

$ pip --version
pip 9.0.1 from /Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages (python 3.6)

$ python2 --version
Python 2.7.13

$ pip2
pip 9.0.1 from /usr/local/lib/python2.7/site-packages (python 2.7)

```

You are welcome ;-)
