# Linux from Scratch

I'm working with version 8.3.

Important links:
* www.linuxfromscratch.org/lfs/faq.html
* www.linuxfromscratch.org/search.html
* www.linuxfromscratch.org/hints/downloads/files/errors.txt

My first try will follow the book closely.

## Chapter 2
Version check - what I had to change on CentOS 7:
### Correct yacc
sudo yum remove byacc // The system had Berkeley yacc installed
                      // We want /usr/bin/yacc to link to bison
sudo ln -s /usr/bin/bison /usr/bin/yacc
### Correct gcc
sudo yum install centos-release-scl-rh
sudo yum install devtoolset-3-gcc devtoolset-3-gcc-c++
sudo scl enable devtoolset-3 bash
### Correct Texinfo
sudo yum install texinfo
### Correct make
sudo yum install devtoolset-6-make
sudo mv /opt/rh/devtoolset-6/root/bin/make /bin/make

