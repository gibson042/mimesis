<div align="center">
      <a href="https://github.com/lk-geimfari/mimesis">
        <img src="https://raw.githubusercontent.com/lk-geimfari/mimesis/master/media/logo-no-descr.png">
    </a><br><br>
</div>

---


| **`Linux`**  |  **`Windows`**  | **`Docs`**  | **`Coverage`**  | **`PyPi`**   | **`Python`**  |
|---|---|---|---|---|---|
| [![Build Status](https://travis-ci.org/lk-geimfari/mimesis.svg?branch=master)](https://travis-ci.org/lk-geimfari/mimesis) | [![Build status on Windows](https://ci.appveyor.com/api/projects/status/chj8huslvn6vde18?svg=true)](https://ci.appveyor.com/project/lk-geimfari/mimesis) | [![Documentation Status](https://readthedocs.org/projects/mimesis/badge/?version=latest)](http://mimesis.readthedocs.io/?badge=latest) | [![codecov](https://codecov.io/gh/lk-geimfari/mimesis/branch/master/graph/badge.svg)](https://codecov.io/gh/lk-geimfari/mimesis)| [![PyPI version](https://badge.fury.io/py/mimesis.svg)](https://badge.fury.io/py/mimesis)| [![Python](https://img.shields.io/badge/python-3.5%2C%203.6-brightgreen.svg)](https://badge.fury.io/py/mimesis) |


**Mimesis** is a fast and easy to use library for Python programming language, which helps generate synthetic
data for a variety of purposes in a variety of languages. This data can be particularly useful during software development and testing. For example, it could be used to populate a testing database, create beautiful JSON/XML/HTML files, anonymize data taken from a production service, etc.

This library offers a number of advantages over other similar libraries:

* Performance. Significantly [faster](https://gist.github.com/lk-geimfari/e76c12eb3c9a8afbf796c706d4ba779d) than other similar libraries.
* Completeness. Strives to provide many detailed providers that offer a variety of data generators.
* Simplicity. Does not require any modules other than the Python standard library.

## Installation
To install mimesis, simply use pip:

```zsh
➜  ~ pip install mimesis
```

also you can install it manually:

```zsh
(env) ➜ git clone git@github.com:lk-geimfari/mimesis.git
(env) ➜ cd mimesis/
(env) ➜ make install
```

## Documentation
Examples below should help you get started. Complete documentation is available on [Read the Docs](http://mimesis.readthedocs.io/).

## Getting started
That's library is really easy to use and a simple usage example is given below:

```python
>>> from mimesis import Personal
>>> person = Personal('en')

>>> person.full_name()
'Antonetta Garrison'

>>> person.occupation()
'Backend Developer'
```

## Locales
Mimesis currently includes support for 33 different [locales](http://mimesis.readthedocs.io/#id1). You can specify a locale when creating providers and they will return data that is appropriate for the language or country associated with that locale:

```python
>>> from mimesis import Personal

>>> de = Personal('de')
>>> pl = Personal('pl')

>>> de.full_name()
'Sabrina Gutermuth'

>>> pl.full_name()
'Światosław Tomankiewicz'
```

## Data providers

Mimesis support over twenty different [data providers](http://mimesis.readthedocs.io/#id2) available, which can produce data related to food, people, computer hardware, transportation, addresses, and more.

## How to Contribute
1. Take a look at [contributing guidelines](https://github.com/lk-geimfari/mimesis/blob/master/CONTRIBUTING.md).
2. Check for open issues or open a fresh issue to start a discussion around a feature idea or a bug.
3. Fork the repository on GitHub to start making your changes to the *your_branch* branch.
4. Add yourself to the list of [contributors](https://github.com/lk-geimfari/mimesis/blob/master/CONTRIBUTORS.md).
5. Send a pull request and bug the maintainer until it gets merged and published.

## License
Mimesis is licensed under the MIT License. See [LICENSE](https://github.com/lk-geimfari/mimesis/blob/master/LICENSE) for more information.

## Disclaimer
The authors assume no responsibility for how you use this library data generated by it. This library is designed only for developers with good intentions. Do not use the data generated with Mimesis for illegal purposes.
