# ga: Google Authenticator in the Shell

This give you a command to generate two factor authentication codes
that are compatible with Google Authenticator from the shell.

## References

[RFC6238](https://tools.ietf.org/html/rfc6238)

## Installing

Just install `ga` somewhere on your path (e.g., `$HOME/bin`).

Requirements:
* gnupg

Optional dependencies:
* xclip - to send login codes to the X clipboard instead of stdout
* xorg-xwd, zbar - to parse QR codes from screen with -c option
* qrencode, imagemagick - to display QR codes with -v option

## Using

* `ga [-x]  service` - get token for service
* `ga -[x]c service` - record seed for new service
* `ga -[x]v service` - view qrcode for service
* `ga -l` - list services setup

The `-x*` flags disable use of X11 even when `$DISPLAY` is set.

## Get involved!

We are happy to receive bug reports, fixes, documentation enhancements,
and other improvements.

Please report bugs via the
[github issue tracker](http://github.com/scslab/ga/issues).

Master [git repository](http://github.com/scslab/ga):

* `git clone git://github.com/scslab/ga.git`

## Authors

David Mazi&egrave;res.

## Copying

Copyright 2014 David Mazi&egrave;res.  You may use and distribute this
code under the terms of the
[GPLv3](http://www.gnu.org/licenses/gpl-3.0.html) or later, and
additionally you may link against openssl libcrypto.

This program comes with ABSOLUTELY NO WARRANTY.  This program REDUCES
YOUR SECURITY by making two-factor authentication not really two
factor.  You may decide using this program is useful where the
alternative is only one factor authentication, but that is your
decision alone.  The author DOES NOT REPRESENT THIS SOFTWARE AS MORE
SECURE THAN ANY ALTERNATIVE; it most likely is less secure.

