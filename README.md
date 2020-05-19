# Ipopt
this is download from https://www.coin-or.org/download/source/Ipopt/
official github repository https://github.com/coin-or/Ipopt

## Basic Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1(mac, linux), 3.81(Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets), only need to be downloaded when you run udaciy mpc project
  * Run either `install-mac.sh` or `install-ubuntu.sh`.
  * If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets
    cd uWebSockets
    git checkout e94b6e1
    ```
* python and matplotlib
  ```
  sudo apt-get install python-matplotlib
  sudo apt-get install python2.7-dev
  ```
    Some function signatures have changed in v0.14.x. See [this PR](https://github.com/udacity/CarND-MPC-Project/pull/3) for more details.

# Installation
 
## Method1:

* using udacity install_Ipopt script, Please refer to [this document](https://github.com/udacity/CarND-MPC-Project/blob/master/install_Ipopt_CppAD.md) for installation instructions.

## Method2:
	
### 1.  sudo apt-get install libblas3 libblas-dev liblapack3 liblapack-dev gfortran
	sudo apt-get install python-numpy (this is for matlibplot c++ verison)

### 2.  using apt-get to install ASL Mumps
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

### 3.  after installed dependecy, you can install Ipopt(version: 3.12.7)
	$ wget https://www.coin-or.org/download/source/Ipopt/Ipopt-3.12.7.zip 
	$ unzip Ipopt-3.12.7.zip 
	$ rm Ipopt-3.12.7.zip
	$ cd Ipopt-3.12.7
	$ ./configure
		......
		configure: Main configuration of Ipopt successful
 
	$ make
	$ make test
	$ make install

### 4.  install Ipopt(verison: 3.13.2)

* IPOPT can be downloaded with:

	git clone -b stable/3.13 https://github.com/coin-or/Ipopt.git CoinIpopt

* Before compiling IPOPT you need hsl. It is not open source, but a free copy can be requested from:

	http://www.hsl.rl.ac.uk/ipopt/ you aslo can find a copy in this repository

* Compile and install hsl as follows:

	a) extract the copresses binaries into some directory DIR/

	b) next move the files from DIR/include into usr/local/include and DIR/lib into usr/local/lib and DIR/lib/pkgconfig into usr/local/pkgconfig

	c) run ldconfig to map the package names to the directory:

	sudo ldconfig

* Now compile and install IPOPT with the following terminal commands:

	cd .../CoinIpopt

	./configure

	make

	make install

	make test

* Make sure the ipopt binaries that end up in /CoinIpopt/lib/ are in /usr/local/lib and copies of related headers from /CoinIpopt/include/coin/ are copied to /usr/local/include/coin.


* After make install, Ipopt3.13 copied /CoinIpopt/include/coin/ to /usr/local/include/coin-or, but cppad in mpc project included head files by "# include <coin/IpIpoptApplication.hpp>", so it cannot find it. Hence, you should mv /usr/local/include/coin-or to /usr/local/include/coin or copy.

* [References](https://github.com/bapaden/ipopt-cmake-demo)  

