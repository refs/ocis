# ownCloud Infinite Scale

[![Build Status](https://cloud.drone.io/api/badges/owncloud/ocis/status.svg)](https://cloud.drone.io/owncloud/ocis)
[![Gitter chat](https://badges.gitter.im/cs3org/reva.svg)](https://gitter.im/cs3org/reva)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/dc97ddfa167641d8b107e9b618823c71)](https://www.codacy.com/app/owncloud/ocis?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=owncloud/ocis&amp;utm_campaign=Badge_Grade)
[![Go Doc](https://godoc.org/github.com/owncloud/ocis?status.svg)](http://godoc.org/github.com/owncloud/ocis)
[![Go Report](http://goreportcard.com/badge/github.com/owncloud/ocis)](http://goreportcard.com/report/github.com/owncloud/ocis)
[![](https://images.microbadger.com/badges/image/owncloud/ocis.svg)](http://microbadger.com/images/owncloud/ocis "Get your own image badge on microbadger.com")

**This project is under heavy development, it's not in a working state yet!**

## Install

You can download prebuilt binaries from the GitHub releases or from our [download mirrors](http://download.owncloud.com/ocis/ocis/). For instructions how to install this on your platform you should take a look at our [documentation](https://owncloud.github.cio/ocis/)

## Development

Make sure you have a working Go environment, for further reference or a guide take a look at the [install instructions](http://golang.org/doc/install.html). This project requires Go >= v1.13.

```console
git clone https://github.com/owncloud/ocis.git
cd ocis

make generate build

./bin/ocis -h
```

## Starting the fullstack server

In order to use micro to access the extensions you'd need to start the runtime first:

```sh
micro
```

That will start:

```sh
❯ micro list services
go.micro
go.micro.api
go.micro.bot
go.micro.broker
go.micro.http.broker
go.micro.monitor
go.micro.network
go.micro.proxy
go.micro.registry
go.micro.router
go.micro.runtime
go.micro.store
go.micro.tunnel
go.micro.web
```

Then start the ocis fullstack server

```sh
./bin/ocis server
```

This starts every extension along with the micro's services:

The resulting state is something like this:

```
go.micro
go.micro.api
go.micro.api.hello
go.micro.bot
go.micro.broker
go.micro.http.broker
go.micro.monitor
go.micro.network
go.micro.proxy
go.micro.registry
go.micro.router
go.micro.runtime
go.micro.store
go.micro.tunnel
go.micro.web
go.micro.web.graph
go.micro.web.hello
go.micro.web.konnectd
go.micro.web.ocs
go.micro.web.phoenix
go.micro.web.webdav
```


## Security

If you find a security issue please contact security@owncloud.com first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2019 ownCloud GmbH <https://owncloud.com>
```
