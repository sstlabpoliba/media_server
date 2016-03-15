# GStreamer RTSP server

## Requirements

- GStreamer 1.7 or upper (please install it compiling the sources)
- autoconf, libtool and C related tools to compile code

## Useful commands

- Install basic deps:

    `sudo apt-get update`
    
	`sudo apt-get install autoconf automake libtool build-essential ubuntu-restricted-extras`
	
	`sudo apt-get install flex bison`

- If you got an *undefined symbol blah blah blah*:

  - `export LD_LIBRARY_PATH=/usr/local/lib`




## Compile program example


`libtool --mode=link gcc -Wall <program.c> -o <executable> -I/usr/local/include/gstreamer-1.0 -I/usr/local/lib/gstreamer-1.0/include -I/usr/include/glib-2.0 -I/usr/lib/x86_64-linux-gnu/glib-2.0/include -I<path_to_gst-rtsp-server>/gst-rtsp-server-1.7.90  -L/usr/local/lib -lgstrtsp-1.0 -lgstreamer-1.0 -lgstsdp-1.0 -lgio-2.0 -lgobject-2.0 -lglib-2.0 -L<path_to_gst-rtsp-server>/gst/rtsp-server/.libs -lgstrtspserver-1.0`
