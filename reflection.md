# Reflection

| Function | Description | Attribute |
| --- | --- |  --- |
| [help](https://docs.python.org/3/library/functions.html#help) | get built-in help | |
| [type](https://docs.python.org/3/library/functions.html#type) | the type of the object | |
| [callable](https://docs.python.org/3/library/functions.html#callable) | check if can be called | \_\_call\_\_ |
| [dir](https://docs.python.org/3/library/functions.html#dir) | list of valid attributes of the object | \_\_dir\_\_ |
| [getattr](https://docs.python.org/3/library/functions.html#getattr) | the value of the named attribute of an object (or default value provided) | |

from inspect import getsource, getfile, getmodule

| Function | Description |
| --- | --- |
| getsource | returns the source code |
| getfile | gets the location of the implementation |
| getmodule | gets module name |
