Mole Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/mole-cash/mole.svg?branch=master)](https://travis-ci.org/mole-cash/mole)

https://mole.cash

What is Mole?
----------------

Mole is an experimental digital currency designed to enable instant payments to anyone, anywhere in the world. This means users can send and receive money quickly without the need for traditional financial intermediaries such as banks or other financial institutions. Mole aims to create a global, borderless, and low-cost payment system.

One of the standout features of Mole is its use of peer-to-peer (P2P) technology. This technology allows the Mole network to operate without a central authority or controlling organization. Instead, all transactions and the issuance of currency are managed collectively by the network of users. This makes Mole a decentralized, transparent, and uncontrolled system by any individual or entity.

Mole Core is the open-source software that serves as the core technological platform for operating the Mole currency. Being open-source, anyone can view, inspect, contribute to, or modify the source code of Mole Core, which enhances the system's transparency and reliability. Mole Core allows users to connect to the Mole network, conduct transactions, and participate in the transaction validation process (if they choose to run a node in the network).

In summary, Mole is a digital currency project aimed at creating a global, fast, low-cost, and decentralized payment system. With peer-to-peer technology and the open-source Mole Core software, this project promises to bring financial freedom and accessibility to people worldwide.

For more information, as well as an immediately useable, binary version of
the Mole Core software, see [https://mole.cash](https://mole.cash).

License
-------

Mole Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/mole-cash/mole/tags) are created
regularly from release branches to indicate new official, stable release versions of Mole Core.

The https://github.com/mole-cash/mole/gui repository is used exclusively for the
development of the GUI. Its master branch is identical in all monotree
repositories. Release branches and tags do not exist, so please do not fork
that repository unless it is for development reasons.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

The developer [mailing list](https://groups.google.com/forum/#!forum/mole-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #mole-dev.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

We only accept translation fixes that are submitted through [Mole Core's Transifex page](https://www.transifex.com/projects/p/mole/).
Translations are converted to Mole periodically.

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.
