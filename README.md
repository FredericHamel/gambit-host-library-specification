# gambit-host-library

Grammar
=======

The unique module name grammar may look like this:
```
HOST_MODULE_NAME ::= HOST/USERNAME/REPO_NAME/TREE_SEP/VERSION/SUBDIR
HOST ::= NAME.NAMEPORT | NAME.HOST
NAMEPORT ::= NAME | NAME:PORT
REPO_NAME ::= NAME
TREE_SEP ::= tree | src | ...  --- This is host dependant.
VERSION ::= INT.INT.INT | TAG_NAME
SUBDIR ::= NAME/NAME | NAME/SUBDIR
```

This is actually the path use to store the downloaded library on the system.

Library location
================
Library location may be specify using ~~pkg in the gambit environment.
An other method would be to use environment variable like GOROOT and GOPATH
in the go library system.

