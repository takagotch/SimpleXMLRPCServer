### SimpleXMLRPCServer
---
https://docs.python.org/3/library/simplexmlrpcserver.html

https://github.com/enthought/Python-2.7.3/blob/master/Lib/SimpleXMLRPCServer.py

```py
import xmlrpclib
from xmlrpclib import Fault
import SocketServer
import BaseHTTPServer
import sys
import os
import traceback
import re
try: 
  import fcntl
except ImportError:
  fcntl = None
  
def resolve_dotted_attribute(obj, allow_dotted_names=True):
  
  if allow_dotted_names:
    attrs = [attr]
    
  for i in attrs:
    if i.startswith('_'):
      raise AttributeError(
        'attempt to access private attribute "%s"' % i
      )
    else:
      obj = getattr(obj,i)
  return obj
  
def list_public_methods(obj):
  object, which represent callable attributes

  return [member for member in dir(obj)
    if not member.startswith('_') amd
      hasattr(getattr(obj, member), '__call__')]

def remove_duplicates(lst):

 




```

```
```

```
```
