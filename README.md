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

There is however a part of it that is quite usable and possibly also useful: [top](https://github.com/tittoassini/top), the typed oriented protocol.

### Included and Related Projects

Quid2's sub projects are:
* [top-apps-ghcjs](https://github.com/tittoassini/top-apps-ghcjs)
  * Example WWW applications for [top](https://github.com/tittoassini/top), using [ghcjs](https://github.com/ghcjs/ghcjs).
* [top-apps](https://github.com/tittoassini/top-apps)
  * Example applications for [top](https://github.com/tittoassini/top).
* [top](https://github.com/tittoassini/top)
  * API for top, the typed oriented protocol.
* [typed](https://github.com/tittoassini/typed)
  * Language independent, absolute types.
* [flat](https://github.com/tittoassini/flat)
  * Principled and efficient serialization.
* [model](https://github.com/tittoassini/model)
  * Derivation of data type models from Haskell data types.

A related project is [router](https://github.com/tittoassini/router), the message router used to implement the [top](https://github.com/tittoassini/top) service.

### Installation

`git clone --recursive https://github.com/tittoassini/quid2.git;cd quid2;stack build`

This will retrieve the whole quid2 suite and build all subprojects except [top-apps-ghcjs](https://github.com/tittoassini/top-apps-ghcjs), as setting up ghcjs takes a long time.

To verify that all works, start up the `top-chat` program:

```
stack exec top-chat

Enter your name:
titto

Help:
To send a message: just enter it and press return.
To exit: Ctrl-D.

Current Subject: (Haskell)

Hello!
```

That's it!

### Support
Problems? Questions? Open an **Issue** on this repository or write directly to *titto* at: *tittoassini@gmail.com*
