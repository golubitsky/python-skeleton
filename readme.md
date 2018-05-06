# Requirements

I want to
* develop Python code in a TDD fashion
* automatically run unit tests on change of any source or test code.

This turns out to not be as simple as it sounds.  
I don't currently care about anything else (like deploying or publishing this code).

# Compromises

Bridges will be crossed as necessary.

This project
* is something I'd like to evolve into an [auto-generator](http://yeoman.io/authoring/) for a Python project
* doesn't use `requirements.txt` (well, mostly because there are no requirements yet)
* uses `__init__.py` in the tests folder, which I've read is not recommended (not sure) -- but it **must** be there as of now!
* is missing a `setup.py` file (I think this is just for [publishing to PyPi](https://packaging.python.org/tutorials/distributing-packages/#setup-py))
* probably breaks a bunch of rules for publishing packages.

# Success

1. Install [pytest-xdist](https://github.com/pytest-dev/pytest-xdist)
2. `git clone` and `cd` into this project
3. Run `pytest -f` to automatically run tests in [looponfailing mode](https://docs.pytest.org/en/3.0.0/xdist.html#running-tests-in-looponfailing-mode) and wait for changes.

According to [pytest's test discovery rules](https://docs.pytest.org/en/latest/goodpractices.html#conventions-for-python-test-discovery), tests have to
* be in a file named `test_*.py` or `*_test.py`
* either
  * be in a method named `test_*`

# Future

As my requirements and knowledge of Python expand I will improve upon this project to further streamline my Pythonic process.