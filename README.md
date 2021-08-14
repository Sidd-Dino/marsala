# Marsala

A notification aggregator based on tiramisu written in bash

![scrot](https://imgur.com/ndbJ2HJ.png)


## Features

```
* Daemon & Client

  Marsala has a daemon and client mode
  The daemon as the word implies runs in the background
  storing the notifciations in a temp direcotry
  The client provides a nice way of viewing them
  ( or just use cat :P )

* Notifications sorting

  The notifications that marsala gathers is sorted based on
  sources.
```


## Dependencies
 - bash 4+
 - tiramisu [source](https://github.com/Sweets/tiramisu)


## CLI Options

```sh
marsala [options]

-D (start daemon)
-h (help)
-v (version)

```

## Keybindings

```
Keys   Function
n ->   next source feed
p <-   prev source feed
r      refresh feed
c      clear the current feed
P      display the current field in a pager
?      goto help

```


## Usage

```sh
$ marsala -D   # Start the daemon

$ marsala      # Start the client
```


## Customisation

```
Customisations are done through envoirment variables

# Path to store temp dir of marsala
# /tmp is chosen as default since it gets cleaned
# on every boot (changes distro to distro)
export MARSALA_TMPDIR=

# Specifies the format that will be pased to the
# -o flag in tiramisu.
# Check the tiramisu README for more info about the
# output formats
export TIRAMISU_FORMAT="#summary"$'\n'"#body"
```

## Why Marsala ?

*An excerpt about tiramisu from wikipedia*
> Traditional tiramisu contains a short list of ingredients:
> finger biscuits, egg yolks, sugar, coffee, mascarpone cheese,
> cocoa powder and sometimes liquor.....
> Among the most common alcoholic changes includes the addition of
> Marsala.



## About my code

It's heaivily influenced to by dylanaraps way of doing things. I fear it might be too much, cos I feel like I'm bordering plagarism. Need to find mah identity
