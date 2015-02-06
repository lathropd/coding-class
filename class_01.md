#Welcome to coding for journalists!

Hi, welcome to python for journalists. If you're not taking this as part of the class, you'll need to go through a few preliminary steps under "[Install Virtual Box](virtualbox.md)". Hopefully for those in the class, you can skip to the section, called "Load iPython Notebook."



###3. Create an iPython notebook

You are now in the iPython notebook. Create a New Notebook then click on its title and change the name to "Week 1".

[![](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.32.45_AM/cfcfbfe6e6cefb41751c011278ac488b.png)](https://datalab-assets.s3.amazonaws.com/media/CACHE/images/markdown/images/Screen_Shot_2015-02-02_at_11.32.45_AM/9a75a095fd0f60b26eba3ce4f9c74bbe.png)

In the command box type:

```python
print("The lede is the key to any newspaper story.")
```

Now click the "play" button. You should see that printed out on the line below and get a new command prompt.

*Congratulations, you are now a programmer.*


###4. Your first real program

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

###5. Math. Sorry.

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


###6. Entering data from the keyboard

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

###7. Make it look a bit nicer

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

###8. Make your own function, so you can use it later

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
