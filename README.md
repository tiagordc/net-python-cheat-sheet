## Reflection

| Command | Description |
| --- | --- |
| help(any) | display available information |
| type(object) | returns the type of the object |
| callable(any) | means anything that can be called. Implements \_\_call\_\_() |
| dir(object) | return a list of valid attributes of the object. Can be overriden by \_\_dir\_\_() |
| getattr(object, "attr") | returns the value of the named attribute of an object. If not found, it returns the default value provided |

from inspect import getsource, getfile, getmodule

| Command | Description |
| --- | --- |
| getsource(any) | returns the source code |
| getfile(any) | gets the location of the implementation |
| getmodule(any) | gets module name |

## Metaclass



## Decorators



## Generators



## Context managers
