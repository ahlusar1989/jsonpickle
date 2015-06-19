# Compare jsonpickle using python-cjson and simplejson #

### Test machine ###
Ubuntu 8.04, Intel Core 2 Duo 2.0GHz, 2.0 GB RAM


### Task ###
Using an in-memory RSS feed that feedparser has parsed, encode then decode feed.  Run 1000 times using [python-cjson](http://pypi.python.org/pypi/python-cjson) and 1000 times using [simplejson](http://www.undefined.org/python/).  The code to run the benchmark is located in src/benchmark.py

### Results ###
```
# python benchmark.py
Using cjson
0.013447819 sec/pass 
Using simplejson
0.019652153 sec/pass 
```

### Reasoning ###
simplejson has definite advantages, especially on Google's App Engine, where external C/C++ python modules are not allowed.  But, as these benchmarks show, cjson, when available is faster.