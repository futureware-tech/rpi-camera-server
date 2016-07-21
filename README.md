# rpi-camera-server
RPi h264-over-http(s) server using only shell +
[socat](http://www.dest-unreach.org/socat/) +
[raspivid](https://www.raspberrypi.org/documentation/usage/camera/raspicam/raspivid.md).

[![License](http://img.shields.io/:license-mit-blue.svg)](http://mit-license.org)
[![Build Status](https://travis-ci.org/dasfoo/rpi-camera-server.svg?branch=master)](https://travis-ci.org/dasfoo/rpi-camera-server)

Simpliest invocation, listen on port 1234:

```shell
$ ./capture-server 1234
```

VLC can be used as:

```shell
# OSX
$ open -a VLC --args http/h264://your_host:your_port/your_password_if_needed
# https/h264 if you specified the certificate and key.

# Linux
$ vlc http/h264:// ... # see above

# Or use your browser: http://your_host:your_port/your_password_if_needed.jpg
# (note .jpg in the end) to see a single shot from raspistill.
```

A systemd service example is provided for convenience.
