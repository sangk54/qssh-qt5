About QSsh
==========

Clone from https://github.com/lvklabs/QSsh
The code is extracted from source code of Qt Creator 4.7.83.


### Compiling QSsh

Prerequisites:
   * Qt5 / Linux
   * On Windows: not test
   * On Mac: not test

Steps:
   * Build libbotan-2
       * I have tried to build libbotan-2 from https://botan.randombit.net/. But it caused a crash when running sftp. Therefore, I use libbotan-2 in qt-creator-master/src/libs/botan.
       * Deploy libbotan-2.a and all header file to a folder (find qt-creator-master/src/libs/3rdparty/botan/src/lib/ -type f -name *.h -exec cp {} /path/to/deploy \; )

   * Build QSsh
       * Edit src/libs/ssh/ssh.pro, set INCLUDE_PATH and LIBS to your libbotan-2
       * Build project with qt5

I will test on Window and Linux and complete this project later.
