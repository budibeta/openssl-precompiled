# openssl-precompiled
Latest version OpenSSL_1_1_1g

builded with
- strawberryperl  http://strawberryperl.com/
- nasm  https://www.nasm.us/pub/nasm/releasebuilds/2.14.02/win64/
- visual studio 2017
- openssl https://github.com/openssl/openssl/

how to build
- download above program
- set path environment variables
- extract openssl to folder
- open visual studio native tool command prompt
- type in visual studio cmd, eg: cd /d G:
- type cd your openssl root, eg: cd G:\\openssl-OpenSSL_1_1_1g
- type code below

x32 Bit MD (require dll to run)
- nmake clean
- perl Configure VC-WIN32 --prefix=G:\out\DLL\x32\Release --openssldir=G:\out\SSL
- nmake test
- nmake install_sw

x32 Bit MT (static, no require dll runtime)
- nmake clean
- perl Configure VC-WIN32 --prefix=G:\out\Lib\x32\Release --openssldir=G:\out\SSL no-shared
- nmake test
- nmake install_sw

x64 Bit MD (require dll to run)
- nmake clean
- perl Configure VC-WIN64A --prefix=G:\out\DLL\x64\Release --openssldir=G:\out\SSL
- nmake test
- nmake install_sw

x64 Bit MT (static, no require dll runtime)
- nmake clean
- perl Configure VC-WIN64A --prefix=G:\out\Lib\x64\Release --openssldir=G:\out\SSL no-shared
- nmake test
- nmake install_sw
