# Arduino SerialTest

Interfacing Java with Arduino

## Why?

I'm definitely not a Java person, but being able to interface your Arduino with Java can be important. For example, you could use it to work with cool projects like [Firmata](http://firmata.org/) or [Processing](http://processing.org/)

## Installation/Setup

The [official instructions](http://arduino.cc/playground/Interfacing/Java) say that if you've installed the IDE, you don't have to set anything else up. I couldn't get that to work, so I went the manual route. Note that the serial port has been changed to work with my board and that yours may be different.

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

## License

MIT. See `LICENSE`.
