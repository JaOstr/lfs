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
### Correct gcc and make
sudo yum install centos-release-scl
sudo yum install devtoolset-7
scl enable devtoolset-7 bash
### Correct Texinfo
sudo yum install texinfo
### Correct patch
sudo yum install patch

