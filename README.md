An umbrella repository for projects related to Quid2.

### What Is Quid2? 

Quid2 (pronounced *[quidquid](https://en.wiktionary.org/wiki/quidquid)*) is a general framework for the definition, preservation and sharing of data.

It is composed by a suite of mini-specifications to:
* create canonical, language independent, data type definitions
* convert canonical data values to and from an efficient and principled binary format
* use a content-oriented transport protocol for large-scale data exchange

### What Can It Do For Me?

Ask not what Quid2 can do for you but rather what you can do for Quid2!

Quid2 is under intense development and not all its parts are currently documented and usable.

At this time the only directly usable project is [quid2-net](https://github.com/tittoassini/quid2-net) so that's where you should [teleport yourself](https://github.com/tittoassini/quid2-net).

### Interested?

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

This will load on your computer the whole quid2 suite and build all subprojects except [quid2-net-apps-ghcjs](https://github.com/tittoassini/quid2-net-apps-ghcjs), as setting up ghcjs takes a long time.

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
