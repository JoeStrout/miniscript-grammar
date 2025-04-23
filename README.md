# MiniScript Grammar

This repo contains the official grammar specification for the [MiniScript](https://miniscript.org) programming language.

It is defined in [ANTLR](https://www.antlr.org/) format, so that it can be machine-verified against sample programs using 
online tools like [ANTLR lab](http://lab.antlr.org/).

## Try it yourself!

To experiment with the grammar online, without having to install or build anything, follow these steps:

1. Go to http://lab.antlr.org/
1. Click on the Lexer tab, and clear out the default lexer content (our lexer rules are part of the main grammar below).
1. Click on the Parser tab, and paste in the contents of [miniscript.g4](miniscript.g4) from this repo.
1. Paste a MiniScript test program (valid or not) into the Input panel on the right.
1. Click the green Run button.

If the input program matches the grammar, you'll see a parse tree (or hierarchy) and no errors.  If it fails, you'll 
see a partial parse, with one or more error messages.

## But why?

MiniScript was developed with a hand-written parser, and never had a formar specification of the grammar, unless you
count the source code of the official reference implementations.  But some users wanted a more digestible and clear
spec, for example, because they were writing their own MiniScript implementation in some other language.

In addition, we are currently preparing for MiniScript 2.0, which will be an entirely clean-sheet implementation
focused on performance.  A clear grammar (along with an extensive test suite, of course) helps ensure that we don't
forget any corner cases.  It also lets us consider minor syntax changes in a safe, organized way, without having
to write a ton of code just to try something out.

And who knows?  Maybe we'll give an ANTLR-generated parser a try.  Even if it doesn't end up being used in MiniScript
2.0, other implementers and tinkerers may appreciate being able to push a button and get most of the parsing done
for them.

For all these reasons, having an official grammar defined in something like ANTLR just makes sense.
