# B O O M

## About

This is a modified version of the [official boom](http://holman.github.com/boom), improved with a list of suggestions when you try to copy or open an item that does not exists (for more details on why I did that [see my blog post](https://medium.com/open-source-life/73489c30e49)).

boom manages your text snippets on your command line. You can stash away text
like URLs, canned responses, and important notes and then quickly copy them
onto your clipboard, ready for pasting.

For more details about what boom is and how it works, check out
[boom's website](http://holman.github.com/boom).

## Install

    # gem install boom
    # nope

If you want to install this version you'll need a few steps as I didn't publish the gem (Ping me if you want me to). So here is how to get it:

    # clone this repo
    $ git clone git@github.com:romainberger/boom.git

    # create the branch and pull it
    $ git co -b did-you-mean
    $ git pull origin did-you-mean

    # build and install the gem
    $ gem build boom.gemspec
    $ gem install boom-0.3.0.gem

## Quick and Dirty

    $ boom gifs
    Boom! Created a new list called "gifs".

    $ boom gifs shirt http://cl.ly/NwCS/shirt.gif
    Boom! "shirt" in "gifs" is "http://cl.ly/NwCS/shirt.gif". Got it.

    $ boom shirt
    Boom! Just copied http://cl.ly/NwCS/shirt.gif to your clipboard.

And that's just a taste! I know, you're salivating, I can hear you from here.
(Why your saliva is noisy is beyond me.) Check out the [full list of
commands](https://github.com/holman/boom/wiki/Commands).


### Did you mean this?

Here is the only thing added to the basic boom version. Let's pretend you want to copy an item called `ridiculously-long-thing`. But you don't quite remember the name. Let's see what happens:

    # How is this thing called again?
    $ boom copy ridiculously-long-stuff
    Couldn't find ridiculously-long-stuff
    Did you mean this?
        ridiculously-long-thing
    # Oooooooh yeah

## Contribute

Want to join the [Pantheon of
Boom'ers](https://github.com/holman/boom/contributors)? I'd love to include
your contributions, friend.

Clone this repository, then run `bundle install`. That'll install all the gem
dependencies. Make sure your methods are [TomDoc](http://tomdoc.org)'d
properly, that existing tests pass (`rake`), and that any new functionality
includes appropriate tests.

The tests are written in shell for
[roundup](https://github.com/bmizerany/roundup), since boom is basically just
Ruby pretending to be shell. `rake` should run them all for you just fine.

All good? Cool! Then [send me a pull request](https://github.com/holman/boom/pull/new/master)!

## I love you

[Zach Holman](http://zachholman.com) made this. Ping me on Twitter —
[@holman](http://twitter.com/holman) — if you're having issues, want me to
merge in your pull request, or are using boom in a cool way. I'm kind of hoping
this is generic enough that people do some fun things with it. First one to use
`boom` to calculate their tax liability wins.
