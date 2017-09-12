# bsdsplash
Add ascii art splash in OpenBSD bootloader. Configured adding ascii &lt;filename> in /etc/boot.conf  

![example.png](./example.png)

# disclaimer
The procedure below is not supported, not recommended, not advisable etc.  
The procedure below will replace the bootloader, if you have no idea what these commands are for, you might end up with an unusable (or not recoverable) system. Learn first how to replace the bootloader.
I will not be responsible in any case.

# license
The files are under BSD license (see header in source file).   
The ascii example is taken from:  
http://www.bsdforen.de/threads/ascii-art-puffy.15717/   
My contribution is related to the Xascii function.

# install
- retrieve OpenBSD sources (stable/current) according to  
[https://www.openbsd.org/faq/faq5.html](https://www.openbsd.org/faq/faq5.html)  
[https://man.openbsd.org/release](https://man.openbsd.org/release)

- merge the files provided here. Do NOT just copy. I will not keep the file updated.

- Assuming you want to install to wd0, compile and install as:

    cd /usr/src  
    make obj  
    cd /usr/src/sys/arch/amd64/  
    make  
    make install  
    installboot wd0   

- add in /etc/boot.conf the file with the desired ascii art

    ascii "filename"




