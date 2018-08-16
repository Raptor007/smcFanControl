This is my **dangerous** fork of the smc-command portion of smcFanControl, which makes it easier to change the SMC fan **maximum speed** rather than just the minimum speed usually adjustable via smcFanControl.  In a way, it is the opposite utility.  I'm personally using this to prevent a broken sensor on my 2007 MacBook Pro from cranking the fans at full speed constantly.

**USE AT YOUR OWN RISK!**  This could seriously harm your computer.  I've only tested this on my 2007 MacBook Pro, and it's possible the SMC values for temperature or fan speed are encoded differently on different Macs.

To build and install:

    cd smc-command
    make
	make install

Intended use is to add this line to the root crontab so it automatically adjusts every minute:

    * * * * * /usr/local/bin/smc -a

To stop using this, remove the line from the crontab **and reboot immediately**.
