# gpio-util

A BASH function named "gpio", which can be used like a simplified version of "gpio" utility in wiringPi library.

Because wiringPi is deprecated and no longer included in Raspbian (Raspberry Pi OS) distribution since the version Bullseye, we remove the dependency of wiringPi from UUGear products' software. To minimize the code modification and reserve the (very small) possibility to use wiringPi again in the future, we define a BASH function named "gpio" in the gpio-util.sh file. After including the gpio-util.sh file (using 'source" command or '.'), your BASH script can call the "gpio" function like the way you previously use the "gpio" utility in wiringPi. Only a small part of arguments are actually supported, and please do not expect the same performance as the real "gpio" utility in wiringPi.

Usage:  
 `gpio [ -g | -1 ] mode/read/write`  
 `gpio readall`  
 `gpio wfi ...`  
  
 Below are some examples of usage:  
  
 `gpio mode 27 up     # set GPIO-27 to input mode and internal pulled up`  
 `gpio read 27        # read GPIO-27 state`  
  
 `gpio mode 27 out    # set GPIO-27 to output mode`  
 `gpio write 27 1     # write GPIO-27 state to high`  
  
 `gpio wfi 27 falling   # wait until GPIO-27 falls`  
  
 `gpio readall       # print information for all GPIO pins`
