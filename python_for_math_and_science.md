#Python for Math, Science, and Pranks

##Before Anything: Don't Break Your Computer

__Good news:__ Python is already installed on your computer, right now! In fact, many of the processes you use every day depend on Python. Depending on what you're using, or how old the document is when you're reading it, it's probably version 2.7.2 or there about. So you can type <code>python</code> and start coding in a python shell right away. Awesome! Python is up to 3.3, but most python developers I know still use 2.7 or even 2.6. This is great for you because.

__Bad News:__ If you install 3.3 or some new python because it's the new thing, and you overwrite the python 2.7 that your computer uses on many of its vital systems, it might use different enough syntax that it breaks tons of stuff. So, if you choose to install 3.3, make sure you're using some kind of version manager.

##Syntax differences from Ruby

Mostly, Python and Ruby syntax are very similar. In this section I'll try to give you enough of the most common differences that you can code some small things without a lot of annoying breaks.

- No end statements

- Put a colon on the end of your for loops.


By the way, for loops:
<pre><code>
for item in list:
  print item * 2
</code><pre>

<pre><code>
list.each do |item|
  print item * 2
end
</code><pre>

While Ruby is always talking about being easy readable, here Python seems much easier. If I told my catsitter "for cat in house: feed cat", she'd understand much easier than if I said "house each do cat feed cat end". You can do for loops in Ruby but you probably never do.

