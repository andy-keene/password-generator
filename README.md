# Simple Password Generator

A standalone python program that generates simple pseudo-random strings. I'm sure there are a dozen versions of this out there, but I didn't care to look and decided to write one myself. Well, you know what they say about security and crypto - always roll your own.

**This should not be used for critical passwords. It's intended to help generate throwaway passwords or phrases.**

## Setup

To use this as a regular command line program:

1. Set the shebang in the `pw` script to the python interpreter you wish to use. Unless you prefer otherwise set this to the path specified by `which python3`.
1. Add `/usr/local/bin` to your `$PATH`, if needed.
1. Set the program files to `rwxr-xr-x`, if needed.
1. Copy the contents of this project to `/usr/local/bin` with `sudo cp -R src/* /usr/local/bin`.
1. Check that `pw` is accessible using `pw --help`.

## Arguments

```
usage: pw [-h] [-l LENGTH] [-d DELIMITER] [-t {mnemonic,alpha_lower,numeric,alpha_numeric}]

optional arguments:
  -h, --help            show this help message and exit
  -l LENGTH, --length LENGTH
                        number of elements to use; defaults to 4
  -d DELIMITER, --delimiter DELIMITER
                        token delimiter to use; defaults to "-"
  -t {mnemonic,alpha_lower,numeric,alpha_numeric}, --token {mnemonic,alpha_lower,numeric,alpha_numeric}
                        type of password tokens to use; defaults to mnemonic words
```

| token name    | set                                                                                                                                                                                                        |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| mnemonic      | [bip-0039](https://github.com/bitcoin/bips/blob/master/bip-0039/english.txt) english word list; used by many wallet programs such as [Electrum](https://electrum.readthedocs.io/en/latest/seedphrase.html) |
| alpha_lower   | [ASCII](https://www.asciitable.com/) lowercase characters (e.g. a-z)                                                                                                                                       |
| alpha_numeric | [ASCII](https://www.asciitable.com/) lowercase characters and digits (e.g. a-z and 0-9)                                                                                                                    |
| numeric       | [ASCII](https://www.asciitable.com/) digits (e.g. 0-9)                                                                                                                                                     |
