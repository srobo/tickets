Srobo Ticket System
===================

Dependencies
------------

 * zbarcam - A QR Code scanning application
    - Only required for scanning a ticket
    - Provided by the Fedora Repos (I've only checked 16) as 'zbar'


Ticket Generation
-----------------

To generate a PDF ticket, all one needs to do is:

    ./generate.py -o <path/to/output/file.pdf> -y 2012 \
                  -d "April 14th-15th" <username>

...where obvious substitutions are made, and assuming 'ticket.key' exists
in the same directory.  If you don't have a 'ticket.key', you can generate
one as follows:

    openssl rand -out ticket.key 256

The ticket used in production should remain both secret and constant.