[![Build Status](https://travis-ci.org/ekristen/prometheus-client.svg?branch=master)](https://travis-ci.org/ekristen/prometheus-client) [![npm](https://img.shields.io/npm/v/prometheus-client-js.svg)](https://www.npmjs.com/package/prometheus-client-js) [![David](https://img.shields.io/david/ekristen/prometheus-client.svg)](https://david-dm.org/ekristen/prometheus-client) [![David](https://img.shields.io/david/dev/ekristen/prometheus-client.svg)](https://david-dm.org/ekristen/prometheus-client#info=devDependencies&view=table)

# Prometheus Client (Pure Javascript)
Originally based https://github.com/StreamMachine/prometheus_client_nodejs, but written without CoffeScript in just JavaScript. (Originally Licensed under Apache 2.0)

[Prometheus](http://prometheus.io) instrumentation metrics library for Node.JS. Metrics are intended to be scraped by a Prometheus server.

![NPM Stats](https://nodei.co/npm/prometheus-client-js.png?downloads=true&downloadRank=true&stars=true)

## Major Changes in V3

There is no more built in HTTP server. The HTTP handler is still available if you'd like to use it but it makes certain assumptions. Like the url will match `/metrics`.

You can grab the metric output manually now by calling `getMetrics` on the instantiated Prometheus Client object.

Version 3 is published as the `next` tag in npm registry. Needs some more testing before officially releasing it.

## Usage

### Getting Started

Install the `prometheus-client` package with NPM:

    npm install prometheus-client-js

Then require the package and set up a new client instance:

```javascript
var Prometheus = require('prometheus-client-js')
var client = new Prometheus()
```

The client library can create an HTTP app to serve up your metrics, or you
can point to the output function from your own app router.

## Metric Types

1. Counter (http://prometheus.io/docs/concepts/metric_types/#counter)
2. Gauge (http://prometheus.io/docs/concepts/metric_types/#gauge)
3. Histogram (http://prometheus.io/docs/concepts/metric_types/#histogram)
