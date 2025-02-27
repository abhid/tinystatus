# Tinystatus

tinystatus generate an html status page via shell script.

## Features

* Parallel checks
* HTTP, ping, port checks
* HTTP expected status code (401, ...)
* Minimal dependencies (curl, nc and coreutils)
* Easy configuration and customisation
* Incident history (manual)

## Demo

An example site is available [here](https://lab.bdro.fr/tinystatus/).

## Setup

To install tinystatus:

* Clone the repository and go to the created directory
* Edit the checks file `checks.list`
* To add incidents or maintenance, edit `incidents.list`
* Generate status page `./tinystatus > index.html`
* Serve the page with your favorite web server

## Configuration file

The syntax of `checks.list` file is:
```
Command | Expected Code | Status Text | Host to check
```

Command can be:
* `http` - Check http status
* `ping` - Check ping status 
* `port` - Check open port status

There are also `http4`, `http6`, `ping4`, `ping6`, `port4`, `port6` for IPv4 or IPv6 only check.

