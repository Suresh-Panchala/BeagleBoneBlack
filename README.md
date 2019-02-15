Building Linux for BeagleBoneBlack ..,!


For Every Successful build of linux kernel, 
The  output  is  like  a  list  of  important  .img,  .dtb  &  binary  files, 
that  are  obtained  from  the  source  and  these  files  are  minimum  required  to  boot  up  your  beagleboard.
___________________________________________________________________________________________________

Getting Started with Build Process :
		
1. Setting up Building Environment and Tools:	


		List of packages and tools that are mandatory to install .. 
        		
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
  	( https://en.wikipedia.org/wiki/BeagleBoard#BeagleBone_Black )
  So, we have to install a Cross-Compiler for ARM Architeture.
		
	command to install ARM Cross-Compiler:
		
		           sudo apt-get install gcc-arm-linux-gnueabi-
		                        (or)
	               sudo apt-get install gcc-arm-linux-gnueabihf-
		   
3. Downloading Source Code and Compiling
    
    Download u-boot:   
        
	ftp://ftp.denx.de/pub/u-boot/u-boot-2019.01.tar.bz2
   
    After Downloading the u-boot ...
    
    	sudo mkdir BeagleBoneBlack && cd BeagleBoneBlack
	      
	Extract downloded u-boot in BeagleBoneBlack directory....
	
		sudo make am335x_boneblack_defconfig
    
    		s
		udo make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi-
		
   this Command will take upto 15 mins to build the image binaries..
   
   the output files that we needed to boot up the beagle are  ( MLO & u-boot.img  https://www.denx.de/wiki/U-Boot/Documentation)
   
   
   After Completion of u-boot
   
   Download Mainline Kernel:
   
    https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.20.10.tar.xz
		

