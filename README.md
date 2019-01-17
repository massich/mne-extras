MNE-EXTRAS
==========

This repo is a collection of gists with utils to use with [mne-python](https://github.com/mne-tools/mne-python).

Usage
-----
```
git clone --recurse-submodules $THIS_REPO mne-extras
cd mne-extras
pip install -e .
```

Then from python we can do:
```py
Python 3.6.6 |Anaconda, Inc.| (default, Oct  9 2018, 12:34:16) 
Type 'copyright', 'credits' or 'license' for more information
IPython 7.1.1 -- An enhanced Interactive Python. Type '?' for help.

In [1]: from mne_extras import write_edf                                                                                                    

In [2]: write_edf?                                                                                                                          
Signature: write_edf(mne_raw, fname, picks=None, tmin=0, tmax=None, overwrite=False)
Docstring:
Saves the raw content of an MNE.io.Raw and its subclasses to
a file using the EDF+ filetype
pyEDFlib is used to save the raw contents of the RawArray to disk

Parameters
----------
mne_raw : mne.io.Raw
    An object with super class mne.io.Raw that contains the data
    to save
fname : string
    File name of the new dataset. This has to be a new filename
    unless data have been preloaded. Filenames should end with .edf
picks : array-like of int | None
    Indices of channels to include. If None all channels are kept.
tmin : float | None
    Time in seconds of first sample to save. If None first sample
    is used.
tmax : float | None
    Time in seconds of last sample to save. If None last sample
    is used.
overwrite : bool
    If True, the destination file (if it exists) will be overwritten.
    If False (default), an error will be raised if the file exists.
File:      ~/repos/mne-extras/mne_extras/edf/save_edf.py
Type:      function

```

What did I do
-----------------
1 - Add the gist as submodule
```
git submodule add https://gist.github.com/bc660ef59dca0dbd53f00ed38c42f6be.git edf
```

2 - Edit `mne_extras/__init__.py` to expose the functionlity


TODO
----
Convert `What did I do` into `how to add a gist to the collection`


