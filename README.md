# Nanopore_rsync
Live sync basecalled Nanopore reads from computer running the MinION to a server or location of your choice

This script was created to work on Mac computers which save MinION basecalled reads to /Library/MinKNOW/data/reads/pass

It utilizes the rsync package using the recursive (-r) and time (-t) flags allowing it to sync files in sub directories
and to prompted to re-run every 30 minutes (1800). 

Choosing target and destination files.  The syntax is as follows.
$ rsync /path/to/target /path/to/destination

This pretty much covers it.  Happy poreing.
