# Python-Concepts
## Content
- [Try and Except](#tryexcept)
- [dunder str, repr](#strrepr)


> <a name = "tryexcept">Try and except</a>

Python has many built in exceptions that are raised when your program encounters an error. When exception occur, the python interpreter stops the current process and passes it to the calling process until it is handled. If not handled the program will crash.

The critical operation which can raise an exception is placed inside the **try** clause. The code that handles the exceptions is written in the **except** clause.


```python
try:
    f = open('test_file.txt')
    var = bad_var
except FileNotFoundError:
    print("Sorry, This file does not exist")
except Exception as e:
    print(e)
```

If you want to run a certain block of code if the code block inside try ran without any errors. For that you can use **else** keyword with the try statement. And **finally** clause to executed no matter what and is generally ised to release external resources.

```python

try:				# checking for exception
	f = open('test_file.txt')
except Exception as e:				# run when there is exception
	print(e)
else:				# run when there is no exception
	print(f.read())
	f.close()
finally:		# it will run no matter what
	print("Excecting Finally... ")			
```

We can raise exceptions using the **raise** keyword.
```python
try:
	f = open('currupt_file.txt')
	if f.name == 'currupt_file.txt':
		raise Exception
except Exception:
	print("File currupted")

```
> <a name = "strrepr">__str__ and __repr__</a>

__str__() method returns the string representation of the object.
__repr__() functin return the object representation in string format.

Well, the __str__ function is suppose to return a human-readable format, which is good for logging or to display some information about the object. Whereas, the __repr__ function is supposed to return an "official" string representatin of the object, which can be used to construct the object again.  

```bash
>>> import datetime
>>> now = datetime.datetime.now()
>>> now.__str__()
'2020-12-27 22:28:00.324317'
>>> now.__repr__()
'datetime.datetime(2020, 12, 27, 22, 28, 0, 324317)'
```

```python
# test.py
class Car:
    def __init__(self, wheel, seat):
        self.wheel = wheel
        self.seat = seat

    def __repr__(self):
        return f'repr wheel: {self.wheel}, repr seat: {self.seat}'

    def __str__(self):
        return f'str wheel:{self.wheel}, str seat: {self.seat}'

car_1 = Car(4, 5)
print(car_1.__repr__())
print(car_1.__str__())
print(f'default: {car_1}')

```
```bash
>>>py test.py
repr wheel: 4, repr seat: 5
str wheel:4, str seat: 5
default: str wheel:4, str seat: 5
```
