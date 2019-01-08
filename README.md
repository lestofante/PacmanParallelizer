# PacmanParallelizer
PP is a minimalistic bash script to parallelize Arch Linux's updates download.
It also support many AUR helper as long as they use "-Syu --noconfirm", but is just one line to change and adapt if you need.

# Usage
Simply run pp.sh to run with pacman; if you provide an argument, it will be used as name of the program to use instead of pacman.

# Why
As experiment. This script has been written in one rainy weekend long ago, when I notice I could not fill the bandwith, and after some frustration with my favourite mirror going down and causing a lot of timeout.
Since the download get spread to all the server in mirrorlist, I belive this solution is actually ethical and with minimal overhead.

But it can defenetly be improved!

# TODO
* use a limited number if mirror for file (for example if 20 mirror are enabled with 10 parallel download, use 2 mirror for file)
* use the mirrors in round robin
* use only one mirror for very small file, where connection overhead is significat
* exclude a mirror if a download error occur
* find a better number for parallel download
