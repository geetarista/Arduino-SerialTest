# Arduino SerialTest

Interfacing Java with Arduino

## Why?

I'm definitely not a Java person, but being able to interface your Arduino with Java can be important. For example, you could use it to work with cool projects like [Firmata](http://firmata.org/) or [Processing](http://processing.org/)

## Installation/Setup

If you've installed the IDE, all you have to do is compile and run the example:

```bash
javac -classpath /Applications/Arduino.app/Contents/Resources/Java/RXTXcomm.jar:. SerialTest.java
java -Djava.library.path=. -cp /Applications/Arduino.app/Contents/Resources/Java/RXTXcomm.jar:. SerialTest
```

If you've installed RXTX manually or separately, run these steps:

First, set up the RXTX library:

```bash
curl -O http://rxtx.qbang.org/pub/rxtx/rxtx-2.1-7-bins-r2.zip
curl -O http://blog.iharder.net/wp-content/uploads/2009/08/librxtxSerial.jnilib
unzip rxtx-2.1-7-bins-r2.zip
cp rxtx-2.1-7-bins-r2/RXTXcomm.jar /Library/Java/Extensions
cp librxtxSerial.jnilib /Library/Java/Extensions
```

Then compile and run the example:

```bash
javac SerialTest.java
java SerialTest
```

Note that the serial port has been changed to work with my board and that yours may be different.

## License

MIT. See `LICENSE`.
