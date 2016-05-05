An umbrella repository for projects related to Quid2.

### What Is Quid2? 

Quid2 (pronounced *[quidquid](https://en.wiktionary.org/wiki/quidquid)*) is a general framework for the definition, preservation and sharing of data.

It is composed by a suite of mini-specifications and corresponding reference implementations to:
* create canonical, language independent, data type definitions
* convert canonical data values to and from an efficient and principled binary format
* use a content-oriented transport protocol for large-scale data exchange

### What Can It Do For Me?

Ask not what Quid2 can do for you but rather what you can do for Quid2!

Quid2 is under intense development and not all its parts are currently documented and usable.

There is however a part of it that is quite usable and that you might be interested in ..

### Quid2-Net, a minimalist content-oriented transport protocol

Most widely used Internet transport protocols are point-to-point, think [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) or [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol). 

quid2-net is, on the contrary, a content-oriented protocol.

Data does not flow from A to B but rather all data of the same type flows on a single, globally unique, channel.

Briefly:
* For every data type there is a corresponding channel
* A channels transfer only data values of its associate type
* Anyone can send and receive data values

You can [see it in action](http://quid2.org/app/ui). 

Under the *Channels* tab are listed the currently open channels, every channel has a type and you can see its full definition by clicking on *Definition*.

Definitions are just plain algebraic data types (with a couple of restrictions: data types definitions cannot be mutually recursive and variables can appear only in kind * positions). 

For example, you should see a *Message* channel that is used to implement a simple chat system. Click on *Show Values* to inspect the value being transferred and then use the [chat user interface](http://quid2.org/app/chat) to login and send a couple of messages and see them appear on the channel.

Under the *Types* tab, is the list of types known to the system.

#### Minimalist and Evolvable

quid2-net does not provide any other service beyond full-duplex typed communication, any other service (e.g. identification or encryption) has to be provided by the clients themselves but that can be done easily and independently by simply creating data types that stands for the additional functionality required.

#### Current Implementation

Though quid2-net is eventually meant to develop into an universal, vendor-free tranport protocol, its current incarnation is provided by a single central router.

Channel could in principle be implemented using different network protocols, currently they are based on [websockets](   https://en.wikipedia.org/wiki/WebSocket), so they are full-duplex, HTTP compatible, TCP connections.

#### APIs

Currently the quid2-net API is available only for the [Haskell](http://www.haskell.org) language, see  [quid2-net](https://github.com/tittoassini/quid2-net).

APIs for other programming languages are planned and help would be greatly appreciated.

### How Do I Use It?

Install Quid2 as specified below and then look at [quid2-net-apps](https://github.com/tittoassini/quid2-net-apps) and [quid2-net-apps-ghcjs](https://github.com/tittoassini/quid2-net-apps-ghcjs) for examples of how to develop stand-alone and www applications.

### Included and Related Projects

The sub projects are:
* [quid2-net-apps-ghcjs](https://github.com/tittoassini/quid2-net-apps-ghcjs)
  * Example WWW applications for [quid2-net](https://github.com/tittoassini/quid2-net), using [ghcjs](https://github.com/ghcjs/ghcjs).
* [quid2-net-apps](https://github.com/tittoassini/quid2-net-apps)
  * Example applications for [quid2-net](https://github.com/tittoassini/quid2-net).
* [quid2-net](https://github.com/tittoassini/quid2-net)
  * API for quid2-net, a *simple*, *accurate* and *free* messaging service.
* [typed](https://github.com/tittoassini/typed)
  * Language independent, absolute types.
* [flat](https://github.com/tittoassini/flat)
  * Principled and efficient serialization.
* [model](https://github.com/tittoassini/model)
  * Derivation of data type models from Haskell data types.

A related project is [router](https://github.com/tittoassini/router), the message router used to implement the [quid2-net](https://github.com/tittoassini/quid2-net) service.

### Installation

`git clone --recursive https://github.com/tittoassini/quid2.git;cd quid2;stack build`

This will retrieve the whole quid2 suite and build all subprojects except [quid2-net-apps-ghcjs](https://github.com/tittoassini/quid2-net-apps-ghcjs), as setting up ghcjs takes a long time.

To verify that all works, start up the `quid2-chat` program:

```
stack exec quid2-chat

Enter your name:
titto

Help:
To send a message: just enter it and press return.
To exit: Ctrl-D.

Current Subject: (quid2-net)

Hello!
```

That's it!

### Support
Problems? Questions? Open an **Issue** on this repository or write directly to *titto* at: *tittoassini@gmail.com*
