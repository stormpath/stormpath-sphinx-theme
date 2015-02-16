# stormapth-sphinx-theme

*Stormpath's official Sphinx theme.*


This is a small Sphinx theme, currently based on the
[RTD Theme][].

As we continue to tweak this theme, it will diverge more from the original.


## Usage

To use this them, you'll need to add it as a git submodule into your project.
You'll typically want to put this theme into the `_themes` directory in your
Sphinx project.  Here's how I do it most of the time:

    $ git submodule add https://github.com/stormpath/stormpath-sphinx-theme.git docs/_themes/stormpath

**NOTE**: The last argument is the relative path this theme will be installed
as.  Make sure the past name ends with `stormpath` -- otherwise the usage
instructions below will fail.

Next, you'll need to modify your `conf.py` file, in order to tell Sphinx to use
this newly installed theme.

The relevant settings you need to set are as follows:

    html_theme = 'stormpath'
    html_theme_path = ['_themes']

Once you've got this configured, you should now be able to build your Sphinx
docs using the Stormpath theme!

Simply run:

    $ make html

From inside your `docs` directory to start the build process.


  [RTD Theme]: https://github.com/snide/sphinx_rtd_theme "RTD Theme"
