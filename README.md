# GoBGP: BGP implementation in Go

[![Build Status](https://travis-ci.org/osrg/gobgp.svg?branch=master)](https://travis-ci.org/osrg/gobgp/builds)
[![Slack Status](https://slackin-gobgp.mybluemix.net/badge.svg)](https://slackin-gobgp.mybluemix.net/)

GoBGP is an open source BGP implementation designed from scratch for
modern environment and implemented in a modern programming language,
[the Go Programming Language](http://golang.org/).

## Getting started

Installing GoBGP is quite easy (only two commands!):

```bash
$ go get github.com/VTabolin/gobgp/gobgpd
$ go get github.com/VTabolin/gobgp/gobgp
```

No dependency hell (library, package, etc) thanks to Go.

## Documentation

## Simple CLI EVPN inject

for macadv type

gobgp global rib add -a evpn macadv 32:77:ad:6a:22:a9 192.168.7.109 0 3123927 rd 65534:394 rt 65534:394
encap vxlan mobility 0 color 105553116266496 color 37383395344384 color 17592186055680 nexthop 172.17.50.52
origin igp med 0

color must be at DEC format
for multicast push type

gobgp global rib add -a evpn multicast 172.17.50.52 0 rd 65534:394 rt 65534:394 encap vxlan label 3123927
origin igp pmsi 172.17.50.52,3123927

### Using GoBGP

 * [Getting Started](https://github.com/osrg/gobgp/blob/master/docs/sources/getting-started.md)
 * CLI
  * [Typical operation examples](https://github.com/osrg/gobgp/blob/master/docs/sources/cli-operations.md)
  * [Complete syntax](https://github.com/osrg/gobgp/blob/master/docs/sources/cli-command-syntax.md)
 * [Route Server](https://github.com/osrg/gobgp/blob/master/docs/sources/route-server.md)
 * [Route Reflector](https://github.com/osrg/gobgp/blob/master/docs/sources/route-reflector.md)
 * [Policy](https://github.com/osrg/gobgp/blob/master/docs/sources/policy.md)
 * [FIB manipulation](https://github.com/osrg/gobgp/blob/master/docs/sources/zebra.md)
 * [MRT](https://github.com/osrg/gobgp/blob/master/docs/sources/mrt.md)
 * [BMP](https://github.com/osrg/gobgp/blob/master/docs/sources/bmp.md)
 * [EVPN](https://github.com/osrg/gobgp/blob/master/docs/sources/evpn.md)
 * [Flowspec](https://github.com/osrg/gobgp/blob/master/docs/sources/flowspec.md)
 * [RPKI](https://github.com/osrg/gobgp/blob/master/docs/sources/rpki.md)
 * [Managing GoBGP with your favorite language](https://github.com/osrg/gobgp/blob/master/docs/sources/grpc-client.md)
 * [Using GoBGP as a Go Native BGP library](https://github.com/osrg/gobgp/blob/master/docs/sources/lib.md)
 * [Graceful Restart](https://github.com/osrg/gobgp/blob/master/docs/sources/graceful-restart.md)

### Externals
 * [Tutorial: Using GoBGP as an IXP connecting router](http://www.slideshare.net/shusugimoto1986/tutorial-using-gobgp-as-an-ixp-connecting-router)
 
## Community, discussion and support

We have the [Slack](https://slackin-gobgp.mybluemix.net/) and [mailing
list](https://lists.sourceforge.net/lists/listinfo/gobgp-devel) for
questions, discussion, suggestions, etc.

You have code or documentation for GoBGP? Awesome! Send a pull
request. No CLA, board members, governance, or other mess.

## Licensing

GoBGP is licensed under the Apache License, Version 2.0. See
[LICENSE](https://github.com/osrg/gobgp/blob/master/LICENSE) for the full
license text.
