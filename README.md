Building Linux for BeagleBoneBlack ..,!


For Every Successful build of linux kernel, 
The  output  is  like  a  list  of  important  .img,  .dtb  &  binary  files, 
that  are  obtained  from  the  source  and  these  files  are  minimum  required  to  boot  up  your  beagleboard.
___________________________________________________________________________________________________

Getting Started with Build Process :
		
1. Setting up Building Environment and Tools:	

      There are a list of packages and tools that are mandatory, listed below 
        sudo apt-get install which
        sudo apt-get install sed
        sudo apt-get install make (version 3.81 or any later)
        sudo apt-get install binutils
        sudo apt-get install build-essential (only for Debian based systems)
        sudo apt-get install gcc (version 4.4 or any later)
        sudo apt-get install g++ (versionsudo apt-get install  s  sudo apt-get install udo apt-get install 4.4 o  sudo apt-get install r any later)
    sudo apt-get ins  sudo apt-get install tall   sudo apt-get insta  sudo apt-get install   sudo apt-get install ll     bash
      patch
      gzip
      bzip2
      perl (version 5.8.7 or any later)
      tar
      cpio
      python (version 2.6 or any later)
      unzip
      rsync
      file (must be in /usr/bin/file)
      bc
     
2. Installing Cross Compiler 
