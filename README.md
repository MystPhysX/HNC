Helleniccoin integration/staging tree
================================

http://www.helleniccoin.gr

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2014-2015 Helleniccoin Developers

What is Helleniccoin?
----------------

Helleniccoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 30 minute block targets
 - subsidy halves in 50k blocks
 - ~100 million total coins

The rest is the same as Bitcoin.
 - 500 coins per block
 - 2016 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Helleniccoin client sofware, see http://www.helleniccoin.gr.

License
-------

Helleniccoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Helleniccoin
development team members simply pulls it.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. 

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test helleniccoin-qt.pro
    make -f Makefile.test
    ./helleniccoin-qt_test

