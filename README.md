## My Portfolio
# Mark Morgan Miranda
---

> Install Virtual Environment:
- pip install virtualenv
> Create a Virtual Environment:
- python -m virtualenv env
- python3.6 -m virtualenv env
> Run Virtual Environment on Windows:
- env\Scripts\Activate
> Run Virtual Environment on Linux:
- source env/bin/activate

> other way to install module:
- python.exe -m pip install -U xhtml2pdf

> Create Lib List (Should be inside Virtual ENV were it is running and all lib or app installed)
- pip freeze > requirements.txt

> Install (Run inside Virtual Env and locate the file)
- pip install -r requirements.txt


> Reinstall clear cache
- pip freeze > pip-freeze.txt
- pip install -r pip-freeze.txt --force-reinstall --no-cache-dir

---

> Migrate
- python manage.py makemigrations <APP>
- python manage.py migrate <APP>
- python manage.py migrate <APP> --database=digixlog

---
> How to print the location

``` print("\033[m\033[0;30;47m File \""+ f"{__file__}\", line " + str(inspect.currentframe().f_lineno) + " : def " + sys._getframe(0).f_code.co_name + "\033[m")```

This format is tested to work on Ubuntu, Windows and, Mac having the File followed by path makes it clickable and directly jump to the location 

<https://www.instructables.com/Printing-Colored-Text-in-Python-Without-Any-Module/>
```
\033[32m" + "\033[m
\033[37;0;40m" + "\033[m

\033[code;code;codem  # put 'm' at the last

\033[code;codem  # use semicolon to use more than 1 code

\033[codem

\033[m   # reset
print(f"\u001b]8;;{__file__}:140\u001b\\{'TRANSACTION LIMIT ORDER BEGINS'}\u001b]8;;\u001b\\")

import sys,inspect

print("\033[m\033[0;30;47m File \""+ f"{__file__}\", line " + str(inspect.currentframe().f_lineno) + " : def " + sys._getframe(0).f_code.co_name + "\033[m")
print("\033[m\033[0;37;41m File \""+ f"{__file__}\", line " + str(inspect.currentframe().f_lineno) + " : def " + sys._getframe(0).f_code.co_name + "\033[m")
print("\033[m\033[0;37;41m File \""+ f"{__file__}\", line " + str(inspect.currentframe().f_lineno) + " : " + sys._getframe(0).f_code.co_name+"("+ str(format(sys.exc_info()[-1].tb_lineno))+")")
```
---
Text color | Code | Text style | Code | Background color | Code
 ------------ | ------------- | ------------ | ------------- | ------------ | -------------
Black | 30 | No effect | 0 | Black | 40
Red | 31 | Bold | 1 | Red | 41
Green | 32 | Underline | 2 | Green | 42
Yellow | 33 | Negative1 | 3 | Yellow | 43
Blue | 34 | Negative2 | 5 | Blue | 44
Purple | 35 | |  | Purple | 45
Cyan | 36 | | |  Cyan | 46
White | 37 | |  | White | 47

> XHTML
- rename your .html to .xhtml then apply the below tag changes.
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
```
It is just those times you know you can do it but simply want to copy paste and make few tweaks 😊
