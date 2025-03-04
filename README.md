# OpenGotha2Misc

Simple utilities to help convert
[OpenGotha](http://vannier.info/jeux/gotournaments/opengotha.htm)
data to other formats.

## og2tbl.html

An HTML+JavaScript webpage to convert an OpenGotha `.h9` (or GoDraw `.web`)
file into an HTML table. Combines lastname/firstname into a single field.

Optionally:

  * map club codes to long names
  * rename columns
  * manually tweak the generated table before saving

Not yet implemented:

  * merge rows (i.e. apply `rowspan` to the table)
  * recalculate tiebreaks

