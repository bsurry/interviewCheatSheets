# Pytest Cheatsheet

## Installation
```bash
pip install pytest
```

## Basic Test Structure
```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
```

## Running Tests
```bash
pytest                # Run all tests in current directory
pytest test_file.py   # Run tests in a specific file
pytest -k "keyword"   # Run tests matching keyword
```

## Assertions
```python
assert a == b
assert a != b
assert a in my_list
assert isinstance(obj, MyClass)
```

## Grouping Tests with Classes
```python
class TestMath:
    def test_add(self):
        assert 1 + 1 == 2
    def test_subtract(self):
        assert 2 - 1 == 1
```

## Fixtures
```python
import pytest

@pytest.fixture
def sample_list():
    return [1, 2, 3]

def test_sample_list(sample_list):
    assert 2 in sample_list
```

## Markers
```python
import pytest

@pytest.mark.skip(reason="skip this test")
def test_skip():
    assert False

@pytest.mark.parametrize("a,b,result", [
    (1, 2, 3),
    (2, 3, 5),
])
def test_add(a, b, result):
    assert a + b == result
```

## Useful Options
- `-v` : verbose output
- `-x` : stop after first failure
- `--maxfail=2` : stop after two failures
- `--disable-warnings` : suppress warnings

## Test Discovery
- Test files should be named `test_*.py` or `*_test.py`
- Test functions should start with `test_`
