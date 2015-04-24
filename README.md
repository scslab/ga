# ga : Google Authenticator in the Shell

This give you a command to generate two factor authentication codes
that are compatible with Google Authenticator from the shell.

## References

[RFC6238](https://tools.ietf.org/html/rfc6238)

## Licensing

This library is GPLv3-licensed.

## Installing

Just install on your path both files.

Requirements:
* gnupg

Optional dependencies:
* xclip - to send login codes to the X clipboard instead of stdout
* xorg-xwd, zbar - to parse QR codes from screen with -c option
* qrencode, imagemagick - to display QR codes with -v option

## Using

```
ga [-x]  service   # get token for service
ga -[x]c service   # record seed for new service
ga -[x]v service   # view qrcode for service
ga -l              # list services setup
```

The `-x*` flags disable use of X11 even when `$DISPLAY` is set.

## Get involved!

We are happy to receive bug reports, fixes, documentation enhancements,
and other improvements.

Please report bugs via the
[github issue tracker](http://github.com/scslab/ga/issues).

Master [git repository](http://github.com/scslab/ga):

* `git clone git://github.com/scslab/ga.git`

## Authors

This library is written by David Mazieres <dm@uun.org>.

