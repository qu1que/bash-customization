# bash customization

I got some linux devices like Notebooks, RPi's and SailfishOS Smartphones.
It's anoying working remotly via ssh on this devices when powered by battery, not knowing the battery status.
So i added this cool function to the bash command prompt.
Additionally i added different colors for the prompt for each device and user. 

Add this at the beginning of your .bashrc file or /etc/bashrc for global use.
I found the battery code on a pine64 forum but it had some issues. I fixed it for my best use case.

Btw. since Sailfish OS 4.x update replaces /bin/bash with a symlink to /usr/bin/busybox, 
you have to install gnu-bash to use .bashrc.


<img src="img1.jpg" width="500" align="center"> 

On SailfishOS, fingerterm is the default terminal app. 
There is an odd Problem with the first character of a string value in PS1 prompt.
Maybe it is related to libreadline and the octal escape sequence \001 and \002.
I leads to a wrong color for the first character of a string value when using any character before the string value"
Using havoc as a terminal app will work without problems.
However, if you use fingerterm, you can move the $BATSTT value before the percentage value.
This problem will ocur on SailfishOS/fingerterm only localy on the device. You can use this line instead:

NEW ADDITION:

Based on JimKnopfIoT's original script, and basically copying his code, I have managed to adapt it to also display the CPU temperature. It is tested on several Raspberry Pi models. I don't know if it would work on other types of devices, but it is very likely, simply by changing the initial path, just like the original script.

<img src="img2.png" width="500" align="center"> 
