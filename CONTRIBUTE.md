# Contributing to dobyemail

Thank you for your interest in contributing to dobyemail! This document provides guidelines for contributing to the project and instructions on how to publish the package to PyPI (Python Package Index).

## How to Contribute

1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes and commit them with clear, descriptive messages
4. Push your changes to your fork
5. Submit a pull request to the main repository

## License

This project is licensed under the Apache License 2.0. By contributing to this project, you agree to license your contributions under the same license. Please make sure you understand the terms of the license before contributing.

If you make significant changes or if a new year has started since the last update, please update the copyright year in the LICENSE file.

## Publishing to PyPI

The dobyemail package has been successfully published to PyPI. The current version is 0.1.2. To update the package for future releases, follow these steps:

1. Ensure you have the latest version of the necessary tools:
   ```bash
   pip install --upgrade setuptools wheel twine
   ```

2. Update the version number in `setup.py` to reflect the new version. Always increment the version number when making changes.

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

6. Upload to PyPI:
   ```bash
   twine upload dist/*
   ```

Note: You'll need to have a PyPI account and be added as a collaborator to the project on PyPI to be able to upload the package.

## Code Style

Please follow PEP 8 guidelines for Python code. Use meaningful variable names and add comments where necessary.

## Testing

Before submitting a pull request, make sure all tests pass:

```bash
python -m unittest discover tests
```

If you've added new functionality, please include appropriate tests.

## Documentation

If you've added new features or made significant changes, please update the documentation accordingly. Ensure that the README.md file is kept up-to-date, as it is used as the long description for the package on PyPI.

Thank you for contributing to dobyemail!
