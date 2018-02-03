# Python 2/3 library for http://sporestack.com/

## Installation

Python 3 is recommended, Python 2 support will be removed entirely.

* `pip3 install sporestack || pip install sporestack`

## In action

[![asciicast](https://asciinema.org/a/98672.png)](https://asciinema.org/a/98672)

## Usage

Use the helper application:

```
$ sporestack spawn
```

Spawn a tor relay for 28 days:

```
$ sporestack spawn --launch tor_relay
```

Spawn and pay with Bitcoin Cash (the default):

```
$ sporestack spawn --currency bch
```

**To be on the safe side you should reset the root password once the server is online.**

View available options (osid, dcid, flavor) as a dict.

```
def node_options():
    """
    Returns a dict of options for osid, dcid, and flavor.
    """
```


Spawn a node.

```
def node(days,
         uuid,
         sshkey=None,
         cloudinit=None,
         startupscript=None,
         osid=None,
         dcid=None,
         flavor=None):
    """
    Returns a node

    Returns:
    node.payment_status
    node.end_of_life
    node.ip6
    node.ip4
    node.hostname
    """
```

# Notes

You can use --wallet_command if you don't want to pay by QR codes all the time.

# Example SporeStack files

https://github.com/sporestack/node-profiles

# Deprecation notice

`nodemeup` has been replaced by `sporestack spawn`.

# Licence

[Unlicense/Public domain](LICENSE.txt)
