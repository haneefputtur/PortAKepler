
## Release a new version

To release a new version. You need publish both the js module in NPM and the python module on PyPI.
Version number of the js module **`kelergl-jupyter`** and the python module **`keplergl`** should match

### To release a new version of keplergl-jupyter on NPM:

- Edit version number in `js/package.json`
```
git commit -am "keplergl-jupyter@<version>"
npm login
npm publish
```

### To release a new version of keplergl on PyPI:

- Update version number in  _version.py

```
git add _version.py
git commit -am "keplergl==<version>
```

- Remove dist, build and upload to PyPI
```
rm -r dist
python setup.py sdist
twine upload dist/*
```

### add tags
```
git tag -a <version>-jupyter -m "<version>-jupyter
git push origin master && git push origin <version>-jupyter
```
