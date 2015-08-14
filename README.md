# pkgrestore
Bash script for saving and restoring a list of top-level packages using aptitude

To save a list of top-level packages (does not include dependencies) to a file, run
./pkgrestore with no arguments. Output filename includes hostname of running machine
and date/time, in the form of packages_$HOSTNAME\_$STAMP.lst

To restore, run ./pkgrestore -i packages_XXX_XXX.lst and confirm. This will read the
list file and call aptitude to install all packages in teh list.

This script could be used as part of a hybird backup/ reload approach, all that would
be needed is to archive/ copy the user's home folder, and perhaps some other 
configuration files from /etc/* or wherever.
