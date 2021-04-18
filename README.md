# Foundry VTT module installer

## About

This script allows you to install any number of Foundry VTT modules at once.

The list of modules is extracted from a text file containing links, which can formatted freely. You can use one module
link per line, but the script will find links no matter how they are separated as long as the separator is not valid as
part of a URL.

Patreon member posts with direct links to modules can be used by saving the post as a _.html_-file from your browser.

 This script requires Python 3 and has no dependencies.

## Usage

You can install modules to a temporary directory or directly to your Foundry VTT _/Data/modules/_ directory. The
destination directory must exist.

The _filters_ parameter can be used to only download links with the given keyword(s). Useful if you're using HTML as the
link source as it usually has a lot of irrelevant links.


```
usage: install.py [-h] [--filters [FILTERS [FILTERS ...]]] file destination

python install.py links.txt modules
python install.py --filters dropbox links.html path/to/foundryvtt/Data/modules
```

Restart Foundry VTT after the modules are installed, go to _Add-on Modules_ and click _Update All_ to complete the
installation.