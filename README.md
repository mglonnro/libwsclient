# libwsclient


## Background
WebSocket client library for C, originally written by [payden](https://github.com/payden/libwsclient). 

- Added some memory leak fixes from [morrowind's](https://github.com/morrowind/libwsclient) fork. (mglonnro)

This library abstracts away WebSocket protocol framing for client connections.  It aims to provide a *somewhat* similar API to the implementation in your browser.  You create a new client context and create callbacks to be triggered when certain events occur (onopen, onmessage, onclose, onerror).

## Installation

```
./autogen.sh
./configure && make && sudo make install
```

## Usage

Your best bet for getting started is to look at `test.c` which shows how to connect to an echo server using libwsclient calls.

To link `test.c` against `libwsclient`: 

```
gcc -g -O2 -o test test.c -lwsclient
```

