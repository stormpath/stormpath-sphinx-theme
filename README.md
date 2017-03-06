#Stormpath is Joining Okta
We are incredibly excited to announce that [Stormpath is joining forces with Okta](https://stormpath.com/blog/stormpaths-new-path?utm_source=github&utm_medium=readme&utm-campaign=okta-announcement). Please visit [the Migration FAQs](https://stormpath.com/oktaplusstormpath?utm_source=github&utm_medium=readme&utm-campaign=okta-announcement) for a detailed look at what this means for Stormpath users.

We're available to answer all questions at [support@stormpath.com](mailto:support@stormpath.com).

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
    $ git submodule init
    $ git submodule update

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
