## create python package on pypi.

build project (note the version in setup.py)
```bash
python setup.py sdist bdist_wheel
```

upload to pypi test
```bash
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

install using pypi test (note the version)
```bash
pip install -i https://test.pypi.org/simple/ pyllama==0.0.4
```



[Working Example](https://towardsdatascience.com/build-your-first-open-source-python-project-53471c9942a7)


[NOT Working Example](https://www.codementor.io/@arpitbhayani/host-your-python-package-using-github-on-pypi-du107t7ku)
