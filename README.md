## panoptic

This will be a collection of modules for accessing, storing and retrieving video frames and streams. It is designed to make writing live streaming and recording applications simple and powerful.

## Development

* panoptic is written in Go and is based on gstreamer and glib


### Packages

#### OSX
* Install:
 * [gstreamer runtime](http://gstreamer.freedesktop.org/data/pkg/osx/1.6.0/gstreamer-1.0-1.6.0-x86_64.pkg)
 * [gstreamer development framework](http://gstreamer.freedesktop.org/data/pkg/osx/1.6.0/gstreamer-1.0-devel-1.6.0-x86_64.pkg)
* Run:
 * `PKG_CONFIG_PATH="/Library/Frameworks/GStreamer.framework/Versions/1.0/lib/pkgconfig:$PKG_CONFIG_PATH" go test`
 * `PKG_CONFIG_PATH="/Library/Frameworks/GStreamer.framework/Versions/1.0/lib/pkgconfig:$PKG_CONFIG_PATH" go run client/camrelay.go`

#### Linux
* `sudo apt-get install golang libgstreamer1.0-dev postgresql-9.3 libpq-dev postgis`

### Source
* `go get github.com/revmischa/panoptic`

### Database Init

```
sudo -u postgres createuser $USER
sudo -u postgres createdb -O$USER panoptic
echo "CREATE EXTENSION postgis" | sudo -u postgres psql panoptic
echo "CREATE EXTENSION pgcrypto" | sudo -u postgres psql panoptic
psql panoptic < schema.sql
```

## Design
_(Work in progress)_

## Reading
* [Sample Surveillance Camera App](http://ahiru.eu/~vivia/rpi/app.c)

## Streaming Server
* `sudo apt-get install json-glib-dev libsoup2.4-dev gtk-doc-tools libtool autoconf automake libssl-dev`
