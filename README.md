GeoPatterns
===========

![](https://f.cloud.github.com/assets/1258/2056684/3dc871ee-8ae8-11e3-9864-7285d6bef584.png)

Generate beautiful SVG patterns from a string. This is a Python-port of
[Jason Long][1]'s [Ruby library][2].

[1]: https://github.com/jasonlong/
[2]: https://github.com/jasonlong/geopatterns/

Installation
------------

GeoPatterns is installable via `pip`:

```shell
$ pip install geopatterns
```

Usage
-----

Create a new pattern by initializing `GeoPattern()` with a string and a
generator (the result of this string/generator pair is the above image).

```python
>>> from geopatterns import GeoPattern
>>> pattern = GeoPattern('A string for your consideration.', generator='xes')
```

Currently available generators are:

* `hexagons`
* `overlappingcircles`
* `rings`
* `sinewaves`
* `squares`
* `xes`

Get the SVG string:

```python
>>> print(pattern.svg_string)
u'<svg xmlns="http://www.w3.org/2000/svg" ...
```

Get the Base64-encoded string:

```python
>>> print(pattern.base64_string)
'PHN2ZyB4bWxucz0iaHR0cDov...
```
