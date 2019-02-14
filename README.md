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
			sudo apt-get install g++ 
			sudo apt-get install  patch
			sudo apt-get install gzip
			sudo apt-get install bzip2
			sudo apt-get install perl (version 5.8.7 or any later)
			sudo apt-get install tar
			sudo apt-get install cpio
			sudo apt-get install python (version 2.6 or any later)
			sudo apt-get install unzip
			sudo apt-get install rsync
      
     
2. Installing Cross Compiler Toolchain:

	Cross-Compiler is nothing but, a Compiler which runs in host machine ( Ex : Laptop ) 
	and produce executables for the target machine 
	(Ex : BeagleBone, RaspberryPi, Panda Board, etc.). 
	Choosing and Installing Cross-Compiler is depends upon the Architecture of the target machine,
	that we are going to build the executables.
	
        In this case, the target device BeagleBoneBlack's Architecture is ARM Cortex-A8 
        ( For more info : https://en.wikipedia.org/wiki/BeagleBoard#BeagleBone_Black )
        So, 
