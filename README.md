# OpenGotha2Misc

Simple commandline utilities to help convert
[OpenGotha](http://vannier.info/jeux/gotournaments/opengotha.htm)
data to other formats.

## og2tbl.html

An HTML+JavaScript webpage to convert an OpenGotha `.h9` or (GoDraw `.web`)
file into an HTML table. Combines lastname/firstname into a single field.
Optionally:

  * merge rows (i.e. apply `rowspan` to the table)
  * map club codes to long names
  * remove/rename columns

## [og2tbl](doc/og2tbl.md)

A Perl script to take an `h9` file and convert it into an HTML table
or to JSON. (obsoleted by `og2tbl.html`)

Filters through `column` for plaintext (`-t`) or JSON (`-J`).

