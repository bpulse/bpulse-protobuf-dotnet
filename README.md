# bpulse-protobuf-dotnet

bpulse-protobuf-donet is the model interface which bpulse relies on in order to send messages with pulses
to the collector, it is a mandatory dependency of [bpulse-sdk-donet](https://github.com/bpulse/bpulse-sdk-dotnet) in order to compile it and send messages to the collector.

# Requirements

* Nuget packages (Visual Studio only):
  * Google.Protobuf
  * Google.Protobuf.Tools

## Protocol Buffers 3.1.0 

In order to build this project you need to install nugets Google.Protobuf.Tools and Google.Protobuf on Visual Studio Project, it is very important that you add nugets on your visual studio project with that reference.

### Windows
you must build the application, then go to directory of your project /bpulse-protobuf-csharp\packages\Google.Protobuf.Tools.3.1.0\tools. in tools folder you should find the proto.exe file for several OS including Windows 64x and 86x

now, you run as admin a cmd.exe
write this command: "protoc -I=$SRC_DIR --csharp_out=$DST_DIR $SRC_DIR/addressbook.proto" without quotes and edit your environment variables adding one that points to the proto.exe file folder like **$SRC_DIR**

e.g. **$SRC_DIR**=C:\Documents\Visual Studio 2015\Projects\bpulse-protobuf-csharp\packages\Google.Protobuf.Tools.3.1.0\tools\windows_x64

Then edit your **$DST_DIR** variable with out folder for you class.

e.g. **DST_DIR**=C:\Documents\Visual Studio 2015\Projects\bpulse-protobuf-csharp\src\main

and now edit **$SRC_DIR/addressbook.proto** with directory of your proto file. 

if you want check if the installation was ok by opening a CMD and executing the following command:

```
protoc --version
```
You should see this output:
```
libprotoc 3.1.0
```

# Contact us

You can reach the Developer Platform team at jtenganan@innova4j.com

# License

The Bpulse Protobuf Java is licensed under the Apache License 2.0. Details can be found in the LICENSE file.
