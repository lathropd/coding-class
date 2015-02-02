#Welcome to coding for journalists!

Hi, welcome to python for journalists. If you're not taking this as part of the class, you'll need to go through a few preliminary steps. Hopefully for those in the class, you can skip to the section, called "Enter the Python."


##Install VirtualBox, your computer within an computer

Since everyone is using kinds of computers on different OS versions and may not have administrative rights, we're using a "VirtualBox" to run a virtual "Linux Workstation" on everyone's machine. Trust us, it's not as scary as it sounds.

Go to [virtualbox.org](https://www.virtualbox.org/wiki/Downloads) and download the installer for your operating system. (Note, for those who are in the class, using a work computer, IT has already done this for you.)

<br>
[![VirtualBox Installer](https://datalab-assets.s3.amazonaws.com/media/markdown/images/Screen_Shot_2015-02-02_at_10.41.53_AM.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_10.41.53_AM/00c4bbda89574d216c7f7cf06ac73257.png)


Use this dropbox link [www.not-really-this.com](http://www.not-really-this.com).


Now open VirtualBox (in the Start -> Applications -> VirtualBox in Windows, and in the Applications folder on Mac).


You should see a screen that looks something like this:

<br>
[![VirtualBox Installer](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_10.41.53_AM/9887c72e1664b530d6d4ef54fce33d23.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_10.41.53_AM/00c4bbda89574d216c7f7cf06ac73257.png)

<br>
Now go to the "File" menu and choose "Import Appliance."

<br>
[![import virtual box appliance menu](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.05.59_AM/84160b5be6fd114ce20371b5de3e857e.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.05.59_AM/99a5bbb048aa8ec6f925410dbff25af9.png)

<br>
Choose the "coding-class-virtualbox.ova" file you just downloaded and import it (requires clicking through two dialog boxes).

<br>
[![vbox ova import](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.07.08_AM/795999d431efaf87f1cf17e45422e3a6.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.07.08_AM/6dffcb65b9118213d2f98705edd59d60.png)

<br>

[![vbox import ova file #2](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.08.41_AM/a1f7378eabac1dfd2aa053d9e47619ea.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.08.41_AM/aad6caba774f5480b9a8b920b25cba53.png)

<br>
Start the VirtualBox instance



##Enter the Python

iPython notebook is a tool for displaying and publishing Python scripts. We'll be using it this first week before we learn some more advanced coding tools.
<br>
But to run it, we first need to meet our new friend, the command line.
<br>
Go to the Ubuntu search box (upper left hand icon) and type "terminal" then click the "Terminal" icon.
<br>

[![terminal](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.21.49_AM/408839e35fc47d15afdc589d31a17b37.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.21.49_AM/ebedde05fe5ea26babb0a4ad9189ff03.png)
<br>


In the terminal enter the command.

```bash
ipython notebook
```

<br>


You are now in the iPython notebook. Create a New Notebook then click on its title and change the name to "Week 1".

[![](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.32.45_AM/cfcfbfe6e6cefb41751c011278ac488b.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.32.45_AM/9a75a095fd0f60b26eba3ce4f9c74bbe.png)



In the command box type:

```python
print("The lede is the key to any newspaper story.")
```

Now click the "play" button. You should see that printed out on the line below and get a new command prompt.

*Congratulations, you are now a programmer.*


##Your first real program

All real programs consist of *functions*, *operations*, *variables* and *control structures*. (There are other goodies, but those come later.)

"print()" was a function. You can tell because it's a single word followed by a set of parentheses. Functions take a value, do something with it and can return another value.

Next we're going to create two variables "foo" and "bar" (these are universal examples used in all programming texts.)

In the command box enter:

```python
foo = 10.0
bar = 11.0
```

Click run. You'll get a new box. Nothing appears to have happened, but you've actually stored those two values. This is called _setting variables_.

Top prove it you're going to _call_ the print _function_ on those variables.

```python
print(foo)
print(bar)
```

Now run it.

Pretty cool, right? You always _set_ a _variable_ by typing it's name, a space, an equals sign, another space and the value you want to set.

You can also perform _operations_ on your variables. The most common kind are arithmetic: +,  -, *&nbsp;(times), / &nbsp;(divided by).

For example, we can calculate the percent change. Percent change is always calculated as new minus old, divided by old or:

```python
new_foo = foo + 10.0
new_bar = bar + 5.0

foo_percent = (new_foo - foo)/foo
bar_percent = (new_bar - bar)/bar

print("The change in foo was:")
print(foo_percent)

print("The change in bar was:")
print(bar_percent)
```

Click run. Look at that. Now lets clean up the formats. We're going to use some math and a function called "round()."

```python
foo_percent = round(foo_percent, 4)
print(foo_percent)
bar_percent = round(bar_percent, 4)
print(bar_percent)
```

So here we did three things: we changed the values of foo_percent and bar_percent, we used the _round()_ function and we used the _print()_ function to change display values. Notice how we set variables (_foo_ and _bar_) equal to the result of the fuction _round()_.

If we wanted to round to one decimal point instead of two we'd do this:

```python
foo_percent = round(foo_percent, 3) * 100
print(foo_percent)
bar_percent = round(bar_percent, 3) * 100
print(bar_percent)
```

Next we're going to have you enter the initial and final values of a new variables, _thing1_ and _thing2_. Make thing2 slightly bigger than thing1:

```python
thing1 = input("Please enter an initial value: ")
thing1 = float(thing1)
thing2 = input("Please enter a final value: ")
thing2 = float(thing2)
percent_change = (thing2 - thing1)/thing1
nice_percent = round(percent_change, 3) *  100
print(nice_percent)
```

What's with "int()"? Great question. Python stores different _types_ of _variable_. When you enter texct from the keyboard it comes in as a _string_. But to do math it needs to be an whole number (called 'integer' or _int_) or a decimal number (called 'floating point' or _float_). We use the _float()_ function to try to turn a _string_ into an _float_. We could also use _int()_, but we'd get an error when we tried to enter a decimal point.

Next thing, we're going to try to make that value look a little nice.

```python
print("The value increased by", nice_percent, "percent.")
```

Notice that we passed multiple string to the print function. Each of those is called a _parameter_. The _print()_ function prints all its parameter on one line with a space between each.

Now try running the same thing, but with the second value smaller than the first.

```python
thing1 = input("Please enter an initial value: ")
thing1 = float(thing1)
thing2 = input("Please enter a final value: ")
thing2 = float(thing2)
percent_change = (thing2 - thing1)/thing1
nice_percent = round(percent_change, 3) *  100
print(nice_percent)
print("The value increased by", nice_percent, "percent.")
```
That's a bit wonky, isn't it? Wouldn't it be nicer change the text when thing2 is less than thing1?

That's called a _conditional_ and it requires us to use some formatting.

```python
if thing2 < thing1:
    print("The value decreased by", nice_percent, "percent.")
else:
    print("The value increased by", nice_percent, "percent.")
```

But we still have that nasty "-". Try this:
```python
if thing2 < thing1:
    print("The value decreased by", -1 * nice_percent, "percent.")
else:
    print("The value increased by", nice_percent, "percent.")
```

The colon and the indent underneath is how Python knows that we're trying to decide between multiple options.

Almost done, I promise. The last thing we're going to do is create our own _function_, a bit like _print()_ or _input()_. But this one is going to run our whole calculator for us. We do that using the _def_ statement and indenting everything beneath it.

```python
def calculate_change():
    thing1 = input("Starting value: ")
    thing2 = input("Ending value: ")
    thing1 = float(thing1)
    thing2 = float(thing2)
    percent_change = (thing2 - thing1)/thing1
    nice_percent = round(percent_change, 3) *  100
    if thing2 < thing1:
        print("The value decreased by", -1 * nice_percent, "percent.")
    else:
        print("The value increased by", nice_percent, "percent.")
```

Hey, nothing happened! That's because we've _defined_ a function. Now we need to run it.

```python
calculate_change()
```
