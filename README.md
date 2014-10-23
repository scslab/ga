# ga : Google Authenticator in the Shell

This give you a command to generate two factor authentication codes
that are compatible with Google Authenticator from the shell.

## References

[RFC6238](https://tools.ietf.org/html/rfc6238)

## Licensing

This library is BSD-licensed.

## Installing

Just install on your path both files. If google-auth-code.c is
uncompiled, then `ga` knows how to compile it on-demmand.

## Using

usage:
```
gaa service        # get token for service
gaa -c service     # record seed for new service
gaa -l             # list services setup
```

## Get involved!

We are happy to receive bug reports, fixes, documentation enhancements,
and other improvements.

Please report bugs via the
[github issue tracker](http://github.com/scslab/ga/issues).

Master [git repository](http://github.com/scslab/ga):

* `git clone git://github.com/scslab/ga.git`

## Authors

This library is written by David Mazieres <dm@uun.org>.

