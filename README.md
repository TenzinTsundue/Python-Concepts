# Python-Concepts
## Content
- [Try and Except](#tryexcept)

---
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

