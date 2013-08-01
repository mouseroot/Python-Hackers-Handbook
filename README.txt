Python hackers handbook

ch0. Modules you might not have heard of
========================================

Python is a remarkable language that combines whitespace/tabs with easy to read syntax that almost
any developer can pick up and get going fast among the standard library exists alot of hidden gems
that not many people know exists or have never used ill list the primary ones that really make python
shine

- ctypes
  A foreign function library for python

- marshal
	The internal python object serialization

- zipfile
	Library for working with zipfiles

- select
	Async I/O for sockets

- pdb
	Python debugger

- inspect
	Python object inspector

- code
	Python interpreter base classes

- _winreg
	Windows registry access

- ast
	The python abstract syntax tree module

- imp
	Python import internals

- json
	JSON decoder/encoder support

- shelve
	Python object persistence

- types
	Python built-in types

- struct
	Read strings as packed binary data


ch1. Ctypes
===========

from ctypes import *

cdll - cdel calling convention
- this is how you call relative dlls 

windll - stdcall(Standard Call) calling convention
- this is how you use windows dlls (kernel32,user32,etc)

oledll - COM interface calling convention
- this is how you connect to COM componets

Data Types
----------

char -> c_char/c_byte/c_long
short - > c_short
int -> c_int
long -> c_long
float -> c_float
double -> c_double

Pass by Value/Pointer
byref() -> &
POINTER() -> *

Common Types
------------
WORD -> c_ushort
DWORD -> c_ulong
LPBYTE -> POINTER(c_ubyte)
LPTSTR -> POINTER(c_char)
HANDLE -> c_void_p

Structures 
----------

class STARTUPINFO(Structure):
    _fields_ = [
	("Some parameter",c_int)
    ]



ch2. binary data
================

import struct

pack - packs binary data into a string given a format

unpack - unpacks binary data from a string given a format


byte order size and alignment

@ - Native Native Native
= - Native Standard None
< - little Endian standard none
> - big endian standard none
! - network(= big-endian) standard none

use sys.byteorder to check the endianess of your system


Format characters
------------------

x - pad byte, No value
c - char,string lendgth of 1
b - signed char, int,1
B - unsigned char,int,1
? - Bool,int,1
h - short,int,2
H - unsigned short,int,2
i - int,int,4
I - unsigned int,int,4
l - Long,int,4
L - unsigned long,int,4
q - long long,int,8
Q - unsigned long long,int,8
f - float,float,4
d - double,float,4
s - char[],string
p - char[],string
P - void *,int


ch3. Talking to networks
========================

ch4. Abstract Syntax Trees
==========================

more to come
============
