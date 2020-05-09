# Ipopt
this is download from https://www.coin-or.org/download/source/Ipopt/.
official github repository https://github.com/coin-or/Ipopt

# Installation 
## Method1:
	using udacity install_Ipopt script, you also can find in this reposittory
	[Ref:] ( https://github.com/udacity/CarND-MPC-Project/blob/master/install_Ipopt_CppAD.md)

# Method2:
## Dependency installation
	sudo apt-get install libblas3 libblas-dev liblapack3 liblapack-dev gfortran
	
	using apt-get to install ASL Mumps
	
	asl-doc: documentation for ASL
	asl-tools: command-line tools for ASL
	asl-tools-dbgsym: debug symbols for asl-tools
	libasl-dev: development files for ASL
	libasl0: multiphysics simulation software
	libasl0-dbgsym: debug symbols for libasl0

	libmumps-5.2.1: Direct linear systems solver - parallel shared libraries
	libmumps-5.2.1-dbgsym: debug symbols for libmumps-5.2.1
	libmumps-dev: Direct linear systems solver - parallel development files
	libmumps-ptscotch-5.2.1: Direct linear systems solver - PTScotch-version shared libraries
	libmumps-ptscotch-5.2.1-dbgsym: debug symbols for libmumps-ptscotch-5.2.1
	libmumps-ptscotch-dev: Direct linear systems solver - PTScotch-version development files
	libmumps-scotch-5.2.1: Direct linear systems solver - Scotch-version shared libraries
	libmumps-scotch-5.2.1-dbgsym: debug symbols for libmumps-scotch-5.2.1
	libmumps-scotch-dev: Direct linear systems solver - Scotch-version development files
	libmumps-seq-5.2.1: Direct linear systems solver - non-parallel shared libraries
	libmumps-seq-5.2.1-dbgsym: debug symbols for libmumps-seq-5.2.1
	libmumps-seq-dev: Direct linear systems solver - non-parallel development files
	mumps-test: Example/test binaries using MUMPS
	mumps-test-dbgsym: debug symbols for mumps-test

## Install Ipopt
	wget https://www.coin-or.org/download/source/Ipopt/Ipopt-3.12.7.zip 
	unzip Ipopt-3.12.7.zip 
	rm Ipopt-3.12.7.zip
	cd Ipopt-3.12.7
	./configure

	make
	make test
	make install

	[Ref:] (https://github.com/bapaden/ipopt-cmake-demo)
