[![](https://img.shields.io/pypi/pyversions/getclass.svg?longCache=True)](https://pypi.org/pypi/getclass/)
[![](https://img.shields.io/pypi/v/getclass.svg?maxAge=3600)](https://pypi.org/pypi/getclass/)
[![Travis](https://api.travis-ci.org/looking-for-a-job/getclass.py.svg?branch=master)](https://travis-ci.org/looking-for-a-job/getclass.py/)

#### Install
```bash
$ [sudo] pip install getclass
```

#### Functions
function|`__doc__`
-|-
`getclass.getclass(obj)`|return instance/method/property/classmethod/staticmethod class

#### Examples
```python
>>> from getclass import getclass

>>> class CLS:
    def method(self): pass

    @property
    def property(self): pass

    @classmethod
    def classmethod(cls,x): pass

    @staticmethod
    def staticmethod(x): pass

    def __str__(self): pass

>>> getclass(CLS())
<class __main__.CLS>

>>> getclass(CLS.method)
<class __main__.CLS>

>>> getclass(CLS.property)
<class __main__.CLS>

>>> getclass(CLS.classmethod)
<class __main__.CLS>

>>> getclass(CLS.staticmethod)
<class __main__.CLS>
```

<p align="center"><a href="https://pypi.org/project/readme-md/">readme-md</a> - README.md generator</p>