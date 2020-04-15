Build instructions on Ubuntu 18.04 

-------------------------------------------------------------------------
Build for Linux :

Build requirements:

	sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3

	sudo apt-get install libboost-all-dev

	sudo apt-get install software-properties-common
	sudo add-apt-repository ppa:bitcoin/bitcoin
	sudo apt-get update
	sudo apt-get install libdb4.8-dev libdb4.8++-dev

	sudo apt-get install libminiupnpc-dev

	sudo apt-get install libzmq3-dev

	sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler

	sudo apt-get install libqrencode-dev


Then do :

	cd depends
	make -j4        ( this number depends on the number of CPU cores you have )
	cd ..
	./autogen.sh
	./configure --prefix=$PWD/depends/x86_64-pc-linux-gnu --disable-tests --disable-bench --disable-gui-tests
	make -j4
	make install



The files will be in depends/x86_64-pc-linux-gnu/bin 

You will need to put at least 

	depends/x86_64-pc-linux-gnu/bin

and

	depends/x86_64-pc-linux-gnu/lib

in the same folder for the binaries to work on any linux.
--------------------------------------------------------------------------



Build for windows and OSX :

Follow the documentation in doc folder























