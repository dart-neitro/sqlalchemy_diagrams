Initial revision:
util.py - no dependencies (start point?)
OrderedDict(dict) - inherit from dict
ThreadLocal(object) - using local thread variables
```
# thread.get_ident() == threading.get_ident(),
object.__getattribute__(self, 'tdict')["%d_%s" % (thread.get_ident(), key)]
```

schema.py - abstractions, interfaces (?)
engine as global valiable - resolving conflicts (?)
```
from sqlalchemy.util import *
```
This's a really terrible idea. Imported objects are not explicit.
Broken interfaces - 
```
class Table(SchemaItem):
  def _set_parent(self, schema):
    ...

class Column(SchemaItem):
  def _set_parent(self, table):
    ...

class Sequence(SchemaItem):
  def set_parent(self, column, key):
    ... 
```

SchemaVisitor(object) - Why have pass-es been used here instead of raising exceptions? 
