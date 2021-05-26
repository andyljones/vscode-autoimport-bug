* `pip install -e demo`
* Open the `__init__.py` file in one tab in vscode so that the auto-importer is aware of its contents
* Then open `test.py` and type 'Hello' and wait for the auto-import suggestion.
* Accept the auto-import. The buggy suggestion is
```
from demo.demo import Hello
```
which is bad since the top-level `demo` doesn't have an `__init__.py` so isn't a package that can be imported from. The correct suggestion would be `from demo import Hello`.