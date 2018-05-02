# gambit-host-library

Grammar
=======

The unique library name grammar may look like this:
```
HOST_LIBRARY_NAME ::= HOST/REPO_PATH/TREE_SEP/VERSION/PATH
PATH ::= REPO_NAME | NAME/NAME
REPO_PATH ::= NAME/NAME
HOST ::= NAME.NAMEPORT | NAME.HOST
NAMEPORT ::= NAME | NAME:PORT
REPO_NAME ::= NAME
TREE_SEP ::= tree | src | ...  --- This is host dependent.
VERSION ::= INT.INT.INT | HASH 
  # Local
  # | TAG_NAME 
  | master
SUBDIR ::= NAME | NAME/SUBDIR
```

The github syntax is `HOST/USERNAME/REPO_NAME/tree/VERSION/SUBDIR`
The gitlab syntax is the same as github,
The bitbucket syntax is `HOST/USERNAME/REPO_NAME/src/VERSION/SUBDIR`
The gogs syntax is the same as bitbucket.

The local import syntax is the same as defined in R7RS.
http://www.larcenists.org/Documentation/Documentation0.98/r7rs.pdf

This is actually the path use to store the downloaded library on the system
in the `R7RS_LIBRARY_LOCATION`

Host library example
====================
```
github.com/foo/src/debug/tree/qux
github.com/foo/bar/tree/debug/tree/qux
```

R7RS on R6RS 
============
http://www.schemeworkshop.org/2014/papers/Kato2014.pdf


Library location
================
Library location may be specify using ~~pkg in the gambit environment.
An other method would be to use environment variable like GOROOT and GOPATH
in the go library system.

