# NAME

og2tbl - convert OpenGotha results file to html or json

# SYNOPSIS

og2tbl \[option ...\] \[--\] FILE

    Options:
       -c, --clubmap FILE
       -e, --elide-column NAME[,NAME ...]
       -r, --rename-header OLD=NEW

       -H, --html
       -J, --json

       -h, --help
           --man

# OPTIONS

- **--**

    Terminates option processing; anything after this is the filename
    to be processed, not an option, even if it looks like an option.

- **-c**, **--clubmap**=_FILE_

    Provide mappings from short club code to full name.

- **-e**, **--elide-column**=_NAME_

    Omit columns from the output.

    Either the name in the input file or the normalised name may be used.

    A comma-separated list of names may supplied or the option may be given multiple times.

- **-r**, **--rename-header**=_OLD_=_NEW_

    Rename (normalise) column header name.

    Option may be given multiple times.

    Mappings supplied supplement or override the default mappings.

# DESCRIPTION

TBC.

# ASSUMPTIONS

- only one set of results per file
- columns do not change partway through
- round columns are ordered ascending from left to right
- a comment giving all or a subset of names of the columns precedes the data rows
- if a subset, the additional columns in the data are unused tiebreaks followed by the round results
- sample data indicates some column names get merged (e.g. SOSSOSOS means SOS followed by SOSOS)
- tiebreak columns are ordered left to right by precedence
- unused tiebreak columns appear to the right of used tiebreaks
- unused tiebreak columns may have "NONE" heading
- unlabelled unused tiebreak columns contain only "0" as data
- spaces in names are encoded by underscores which appear nowhere else
- names are split into exactly two columns: lastname firstname
- an absent name part is encoded by a single underscore (consider player "Weed")
- rows are in descending order of final placement of player in the tournament
- ties may be indicated by only the first of such rows being numbered explicitly
- row number is used as opponent number in results columns
- data rows may have a suffix "|"+number indicating EGD PIN

# CHOICES

- some columns names are normalised
- columns are reordered to place rounds after all others
- if short-long club mapping is provided, codes are expanded with unmatched codes placed inside square brackets
- "No Club" is replaced by "-"
- if there are tied placements, an additional column is prefixed
- EGD PIN info is elided

# SEE ALSO

- http://vannier.info/jeux/gotournaments/opengotha.htm
- https://www.europeangodatabase.eu/EGD/

# AUTHOR

Jonathan H N Chin <code@jhnc.org>

# COPYRIGHT AND LICENSE

    Copyright © 2025 by Jonathan H N Chin <code@jhnc.org>.

    This program is free software; you may redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program; if not, write to the Free Software
    Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
