
##Reflection:

help(any)                ->  display available information
type(object)             ->  returns the type of the object
callable(any)            ->  means anything that can be called. Implements __call__()
dir(object)              ->  return a list of valid attributes of the object. Can be overriden by __dir__()
getattr(object, "attr")  ->  returns the value of the named attribute of an object. If not found, it returns the default value provided.

from inspect import getsource, getfile, getmodule
getsource(any)           ->  returns the source code
getfile(any)             ->  gets the location of the implementation
getmodule(any)           ->  gets module name

