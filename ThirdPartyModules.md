# Third Party Module Compatibility #

Please help contribute to jsonpickle by identifying other Python modules that you have found are compatible with jsonpickle, and which modules jsonpickle does not work well for.  We will actively try to adapt jsonpickle to get coverage of other Python modules.

To test a module, ensure that you can recreate an object by reading with jsonpickle.loads() the output of jsonpickle.dumps() on that object.

For example:
```
>>> import feedparser, jsonpickle
>>> doc = feedparser.parse("http://feedparser.org/docs/examples/atom10.xml")
>>> pickled = jsonpickle.encode(doc)
>>> unpickled = jsonpickle.decode(pickled)
>>> doc['feed']['title'] == unpickled['feed']['title']
True
```

## Works with jsonpickle ##
  * [Universal Feed Parser](http://www.feedparser.org/)
  * [CouchDB](http://incubator.apache.org/couchdb/) - JSON acceptable to place in CouchDB
  * [Joose](http://code.google.com/p/joose-js/) - see http://joose-js.blogspot.com/2008/08/joose-now-supports-jsonpickle.html

## Somewhat works with jsonpickle ##
Unknown

## Does not work at all with jsonpickle ##
Unknown