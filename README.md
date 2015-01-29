ctags-elixir
============

[Exuberant CTags](http://ctags.sourceforge.net/) support for the
[Elixir](http://elixir-lang.org/) language.

This means that if you are writing your Elixir code using an editor
that supports Ctags (e.g.  Vim, Emacs, Sublime Text, and many others), you
can easily jump to the definition of any symbol.  Handy for navigating 
your way around a large, unfamiliar source tree.

To enable:
----------

Copy or append this `.ctags` file to your own `~/.ctags`.

Once you have done that, you can build tags for an Elixir app with the usual
ctags command line: cd into your project, and then

    $ ctags -R .

What is this Exuberant Ctags thing and how do I use it?
-------------------------------------------------------

Well, that's a separate topic, really.  But here's a quick start.

Ctags is a tool to make it easier to implement "go to definition" in lots
of different text editors and for lots of different programming languages.
It has parsers for many languages, and it generates a simple `tags` file
that any editor can read in order to find the file and line where a given
symbol is defined.

The original Ctags supported only C (I think).  Exuberant Ctags is a rewrite
that supports many more languages.

**Install Exuberant Ctags**

If you don't already have Exuberant Ctags, [install it](http://ctags.sourceforge.net/).
On OSX, the best way is using [brew](http://mxcl.github.com/homebrew/):

    $ brew install ctags
    
On Windows, the best way is using [chocolatey](https://chocolatey.org/):

    choco install ctags

**Vim**

If you are using the [vim](http://www.vim.org/) editor:

1. Do the above `ctags -R .` command
2. Open an Elixir source file in vim.
3. Put the cursor on any symbol name, and type the `^]` (Control-]) key.
   The cursor will jump to the definition of that symbol.
4. Type `^O` (or `^T`) to return cursor to previous location.

**Sublime Text 2**

If you are using [Sublime Text](http://www.sublimetext.com/), there is a
[package](https://github.com/SublimeText/CTags) you can install that
adds CTags support.  I haven't tried it, but this is what you would do:

1. If you have not already done so, install [Sublime Package
   Control](http://wbond.net/sublime_packages/package_control).
2. From Sublime Text, Cmd-Shift-P, "install package"
3. Pick "CTags" from the list of packages, and install it
4. Put the cursor on any symbol name, and then type `^T^T`.  This
   should jump to the symbol definition.
5. See the rest of the key bindings [here](https://github.com/SublimeText/CTags).

**Other editors**

There are also other editors that support Ctags.  Check your editor's
documentation, or Google for it.

Feedback
--------

Feedback is more than welcome; I'm new to the Elixir language, so I
probably got some things wrong.
