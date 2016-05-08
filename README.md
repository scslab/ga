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

## OS X and GPG Tools

Mac OS X users may be using the [GPG Tools](https://gpgtools.org/)
distribution. For some strange reason, this package doesn't detect when you are
running in a terminal session without a display (e.g., SSH), so by default, it
always launches a GUI for key entry. Which makes `ga` impossible to use over
SSH on OS X.

To fix this, you'll want to tell it to uses a curses display for passpharse entry:

    export PINENTRY_USER_DATA="USE_CURSES=1"

A good way to decide when to export this variable is by detecting it
`SSH_CONNECTION` is a non-empty string.

## Get involved!

We are happy to receive bug reports, fixes, documentation enhancements,
and other improvements.

Please report bugs via the
[github issue tracker](http://github.com/scslab/ga/issues).

Master [git repository](http://github.com/scslab/ga):

* `git clone git://github.com/scslab/ga.git`

## Authors

David Mazi&egrave;res.
