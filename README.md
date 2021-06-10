# Python-Concepts

## Content
- [Try and Except](#tryexcept)

---
> <a name = "tryexcept">Try and except</a>

```python
try:
    f = open('test_file.txt')
    var = bad_var
except FileNotFoundError:
    print("Sorry, This file does not exist")
except Exception as e:
    print(e)
```

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

How to raise exception on your own
```python
try:
	f = open('currupt_file.txt')
	if f.name == 'currupt_file.txt':
		raise Exception
except Exception:
	print("File currupted")

```
