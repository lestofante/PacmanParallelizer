# PacmanParallelizer  
PP is a minimalistic bash script to parallelize Arch Linux's updates download.  
It also support many AUR helper as long as they use "-Syu --noconfirm", but is just one line to change and adapt if you need.  
  
# Usage
Simply run pp.sh to run with pacman; if you provide an argument, it will be used as name of the program to use instead of pacman. 
  
EXAMPLE  
Using pacman:  
```pp.sh```  
Using trizen (will install AUR, but those download are NOT parallelized):  
```pp.sh trizen```  
  

# Why  
As experiment. This script has been written in one rainy weekend long ago, when I notice I could not fill the bandwith, and after some frustration with my favourite mirror going down and causing a lot of timeout.  
Since the download get spread to all the server in mirrorlist, I belive this solution is actually ethical and with minimal overhead.   
  
Some advantages of using multiple mirror, shuffled random every launch, and multiple are used for download:  
 - if one mirror is down, it will download from the other without timing out each time  
 - if one mirror is not syncronized, it will download from the other without issue  
 - if one mirror is slow, it will download from the others  
 - if by chances all mirror in use are slow, kill and run again so you get a different grouping  
  
But it can defenetly be improved!  
PR are very welcome!  
  
# TODO  
* use only one mirror for very small file, where connection overhead is significat  
* exclude a mirror if a download error occur  
* find a better number for parallel download  
