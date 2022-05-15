# A Tiny patch to Ipython to enable parsing of docstrings when you call Object? or %pinfo Object

When you do `Object?` in Jupyter or Ipython, `pinfo` is the name of the magic command that gets called. This fork adds a couple experimental lines of code to parse the docstring from whatever it currently is, into the NUMPYDOC format which is a bit more readable than say reStructuredText. The before and after looks like this:

![A screenshot of a docstring being displayed in rST format and then in NUMPYDOC format after parsing](https://github.com/TomHodson/ipython/blob/master/before_after.png?raw=true)

I will likely let this get out of sync with the upstream Ipython repo, so if you want to use this I suggest you make your own fork of the IPython repo and manually apply [the 3 line patch](https://github.com/TomHodson/ipython/commit/afc9571a3794d15a7fdf724ed151dc279824f2ad) on top. However if you do want to install this version, do
``` bash
$ git clone https://github.com/TomHodson/ipython.git
$ cd ipython
$ pip install -e '.[test]'
```
