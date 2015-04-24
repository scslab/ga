# ga: Google Authenticator in the Shell

Generate two factor authentication codes that are compatible with
Google Authenticator (a.k.a. RFC6238 TOTP) from the shell.

## References

[RFC6238](https://tools.ietf.org/html/rfc6238)

## Installing

Just download and install
[`ga`](https://raw.githubusercontent.com/scslab/ga/master/ga)
somewhere on your path (e.g., `$HOME/bin/ga`).

Requirements:

* gnupg

Optional dependencies:

* xclip - to send login codes to the X clipboard instead of stdout
* xorg-xwd, zbar - to parse QR codes from screen with -c option
* qrencode, imagemagick - to display QR codes with -v option

## Using

* `ga [-x]` _service_ - get token for _service_
* `ga -[x]c` _service_ - record seed for new _service_
* `ga -[x]v` _service_ - view qrcode for _service_
* `ga -l` - list services setup

The `-x`, `-xc`, and `-xv` flags disable use of X11 even when
`$DISPLAY` is set, compared to no option, `-c`, and `-v`.

## Get involved!

We are happy to receive bug reports, fixes, documentation enhancements,
and other improvements.

Please report bugs via the
[github issue tracker](http://github.com/scslab/ga/issues).

Master [git repository](http://github.com/scslab/ga):

* `git clone git://github.com/scslab/ga.git`

## Authors

David Mazi&egrave;res.
