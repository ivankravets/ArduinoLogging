# Logging library for Arduino and Libelium Waspmote
by Fabrice Jammes - 2016

Forked from https://github.com/mrRobot62/Arduino-logging-library

# Description

Easy to use logging library, like log4j or log4net:
* provide a logger object, and methods like `Error, Info, Warn, Debug, Verbose` to log informations over RS232.
* messages with level below current loglevel are not printed out.
* allow to work with variable argument lists during output.

# Install procedure 

```shell
# for Libellium Waspmote
cd <ide-install-path>/waspmote-pro-ide-v04-linux64/libraries
sudo git clone git@github.com:fjammes/ArduinoLogging.git
cd ArduinoLogging
git ckeckout waspmote
```

```shell
# for Arduino M0 Pro
cd $HOME/Arduino/libraries
sudo git clone git@github.com:fjammes/ArduinoLogging.git
```

Open example project which is included in the `example` directory. Try it, like it :-)

# Major benefits:

## Use formated strings with wildcards

|Wildcard	|Comment	|Example 			|
|-----------|-----------|-------------------|
|%s |replace with an string (char*) |logger.Info("String %s",myString); |
|%c |replace with an character |logger.Info("use %c as input",myChar); |
|%d |replace with an integer value |logger.Info("current value %d",myValue); |
|%l |replace with an long value |logger.Info("current long %l",myLong); |
|%x |replace and convert integer value into hex |logger.Info ("as hex %x), myValue); |
|%X |like %x but combine with 0x123AB |logger.Info ("as hex %X), myValue); |
|%b |replace and convert integer value into binary |logger.Info ("as bin %b), myValue); |
|%B |like %x but combine with 0b10100011 |logger.Info ("as bin %B), myValue); |
|%t |replace and convert boolean value into "t" or "f" |logger.Info ("is it true? %t), myBool); |
|%T |like %t but convert into "true" or "false" |logger.Info ("is it true? %T), myBool); |

