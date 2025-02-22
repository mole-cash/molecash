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

The `main` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
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

Testing and code review are critical components of the development process, but they have become a significant bottleneck in our workflow. The volume of pull requests we receive far exceeds our capacity to thoroughly review and test them in a timely manner. This situation creates delays and challenges in maintaining the pace of development while ensuring the quality and security of the codebase.

Given the nature of this project, which is highly security-sensitive, every line of code must be meticulously examined to prevent vulnerabilities that could potentially lead to severe financial consequences for users. A single oversight or mistake could result in substantial monetary losses, making the review and testing process even more crucial.

To address this bottleneck, we kindly ask for your patience and cooperation. If you have the capacity, please consider contributing by testing other people's pull requests. Your efforts in reviewing, testing, and providing feedback on proposed changes will not only help speed up the process but also enhance the overall reliability and security of the project. Collaborative efforts like these are essential in maintaining the integrity of a project where the stakes are so high.

Remember, this is a community-driven initiative, and every contribution, no matter how small, plays a vital role in ensuring the project's success and safeguarding the interests of its users. Thank you for your understanding and support.

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
