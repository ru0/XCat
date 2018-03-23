## XCat

XCat is a command line program that aides in the exploitation of blind XPath injection vulnerabilities.

### Example:

https://github.com/orf/xcat_app

$xcat http://127.0.0.1:4567 query query=Lawyer --true-string="Rogue"


## Fix Bugs

comment lines in the requester.py.
```
#for param in params:
#    params[param] = quote(params[param], safe='')
```

###  TypeError: cannot use a string pattern on a bytes-like object
modifiy the ansitowin32.py.
```
def write(self, text):
    if(isinstance(text, bytes)):
        self.__convertor.write(text.decode('utf-8'))
    else:
        self.__convertor.write(text)
```