Ctypes
------
```
from ctypes import *
```
+ cdll - cdel calling convention this is how you call relative dlls

+ windll - stdcall(Standard Call) calling convention this is how you use windows dlls (kernel32,user32,etc)

+ oledll - COM interface calling convention this is how you connect to COM componets

Data Types
----------

+ char -> c_char/c_byte/c_long
+ short - > c_short
+ int -> c_int
+ long -> c_long
+ float -> c_float
+ double -> c_double

Pass by Value/Pointer
+ byref() -> &
+ POINTER() -> *

Common Types
------------
+ WORD -> c_ushort
+ DWORD -> c_ulong
+ LPBYTE -> POINTER(c_ubyte)
+ LPTSTR -> POINTER(c_char)
+ HANDLE -> c_void_p

Structures 
----------
```
class STARTUPINFO(Structure):
  _fields_ = [
		("Some parameter",c_int)
	]
```


