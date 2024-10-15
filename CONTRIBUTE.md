# Contributing to dobyemail

Thank you for your interest in contributing to dobyemail! This document provides guidelines for contributing to the project and instructions on how to publish the package to PyPI (Python Package Index).

## How to Contribute

1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes and commit them with clear, descriptive messages
4. Push your changes to your fork
5. Submit a pull request to the main repository

## Publishing to PyPI

To publish the dobyemail package to PyPI, follow these steps:

1. Ensure you have the latest version of the necessary tools:
   ```bash
   pip install --upgrade setuptools wheel twine
   ```

2. Update the version number in `setup.py` if you've made any changes.

3. Clean up any old builds:
   ```bash
   rm -rf build dist *.egg-info
   ```

4. Build the package:
   ```bash
   python setup.py sdist bdist_wheel
   ```

5. Check the package:
   ```bash
   twine check dist/*
   ```

6. Upload to TestPyPI first to ensure everything works correctly:
   ```bash
   twine upload --repository testpypi dist/*
   ```

7. Install from TestPyPI to verify the package works:
   ```bash
   pip install --index-url https://test.pypi.org/simple/ dobyemail
   ```

8. If everything looks good, upload to the real PyPI:
   ```bash
   twine upload dist/*
   ```

Note: You'll need to have a PyPI account and be added as a collaborator to the project on PyPI to be able to upload the package.

## Code Style

Please follow PEP 8 guidelines for Python code. Use meaningful variable names and add comments where necessary.

## Testing

Before submitting a pull request, make sure all tests pass:

```
python -m unittest discover tests
```

If you've added new functionality, please include appropriate tests.

## Documentation

If you've added new features or made significant changes, please update the documentation accordingly.

Thank you for contributing to dobyemail!
