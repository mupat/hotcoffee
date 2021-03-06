hotcoffee
==============================

[![Build Status](https://travis-ci.org/kr1sp1n/hotcoffee.svg?branch=master)](https://travis-ci.org/kr1sp1n/hotcoffee)
[![Coverage Status](https://coveralls.io/repos/kr1sp1n/hotcoffee/badge.svg?branch=master)](https://coveralls.io/r/kr1sp1n/hotcoffee?branch=master)
[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=krispin&url=https://github.com/kr1sp1n/hotcoffee&title=hotcoffee&language=coffeescript&tags=github&category=software)

REST API that saves everything you can imagine.
You just think about a collection name and add an item to it by sending a POST request with body data.
Then you can manipulate items of a collection.


Install
-----------------------------

```bash
git clone git://github.com/kr1sp1n/hotcoffee.git
cd hotcoffee
make install
```


Run Tests
-----------------------------

```bash
make test
```


Start the example server
-----------------------------

```bash
./node_modules/.bin/coffee example/simple_server.coffee
```


Usage
-----------------------------

### GET a list of all collections

```bash
curl http://localhost:1337/
```

__Response__ would be an empty JSON array as long as you never added an item to any collection.

```JSON
[]
```


### POST a new item to a collection

```bash
curl -X POST -d "name=Donatello&color=purple" http://localhost:1337/turtles
```

__Response__

```JSON
{
  "name": "Donatello",
  "color": "purple"
}
```
