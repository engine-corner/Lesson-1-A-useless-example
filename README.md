# A useless example

This is an example of the absolute minimum needed to create an OpenSSL
engine using autoconf, automake and libtool

## Build

Build as follows:

    $ autoreconf -i
    $ ./configure
    $ make

A quick and easy test goes like this:

    $ OPENSSL_ENGINES=.libs openssl engine -t -c useless

Considering this engine has no futher use, we'll stop here.
