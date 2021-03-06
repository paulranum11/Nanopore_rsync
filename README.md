# Nanopore_rsync
Live sync basecalled Nanopore reads from computer running the MinION to a server or location of your choice.


Installing rsync:
  YOU MUST INSTALL "rsync" AND ADD IT TO YOUR PATH ON BOTH THE LOCAL AND DESTINATION MACHINES FOR THIS TO WORK.
  
Installing rsync on Mac (using homebrew):
# Install Homebrew.  Here is a link to their website for reference... you dont need to go here (https://brew.sh).
# Open Terminal 
# and type the following after the prompt
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Install rsync
$ brew install rsync

# link rsync
$ brew link rsync

# Test rsync to see if it was installed and is accessible
$ which rsync

# You should see something like this
$ which rsync
usr/bin/rsync

# To view the rsync documentation type 
$ rsync -h

# Using Nanopore_rsync
# Save Nanopore_rsync to your desktop.
# Navigate to your desktop in terminal
$ cd ~/Desktop

# Make sure that Nanopore_rsync is executable
$ chmod +x Nanopore_rsync

# Now we will add your source and destination directories.  The syntax for this is as follows:
$ rsync /path/to/target /path/to/destination

# Using a text editor specify your source folder (the location to which MinKNOW saves its .fast5 or .fastq read files)
The default is 
/path/to/source

You need to edit this to your source folder like the following example
/Library/MinKNOW/data/reads/20170526_2032_Run6_5_26_2016_FAH04563/fastq/pass

# Using a text editor specify your destination folder (the location to which you would like to copy your nanopore output)
The default is 
/path/to/destination 

You need to edit this to your destination folder like the following example
/Volumes/MORL/Analysis/ranum/Nanopore/Run6

# After entering your destination folder save the Nanopore_rsync document.
# Now you are ready to run Nanopore_rsync
$ bash Nanopore_rsync


This script was created to work on Mac computers which save MinION basecalled reads to /Library/MinKNOW/data/reads/pass

It utilizes the rsync package using the recursive (-r) and time (-t) flags allowing it to sync files in sub directories
and to prompted to re-run every 30 minutes (1800). 

This pretty much covers it.  Happy poreing.
- Paul Ranum
