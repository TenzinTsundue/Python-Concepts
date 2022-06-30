# Python string methods
1. Capitalize
```python
>>> name = 'tenzin'
>>> name_new = name.capitalize()
>>> name_new
'Tenzin'
```
2. casefold
```python
>>> txt = "One Does NOT simpLY Walk"
>>> x = txt.casefold()
>>> x
'one does not simply walk'
```
3. center
```python
>>> name = "Tenzin"
>>> name_new = name.center(10, "_")
>>> name_new
'__Tenzin__'
```
4. count
```python
>>> advice = "Watch The Office"
>>> f_count = advice.count('f')
>>> f_count
2
```
5. Encode
```python
>>> txt = "Mr Stale"
>>> new = txt.encode('ascii', 'ignore')
>>> new
b'Mr Stale'
```
6. Endswith
```python
>>> name = "Michael"
>>> end = name.endswith("ael")
>>> end
True
```
7. expandtabs
```python
>>> txt = "H\tT\tM\tL"
>>> x = txt.expandtabs(5)
>>> x
'H    T    M    L'
```
8. Find
```python
>>> txt = "pineapple on Pizza!"
>>> x = txt.find("a")
>>> x
4
```
9. Format
```python
>>> txt = "I {} The {}".format("love", "Office")
>>> txt
'I love The Office'
>>> txt = "I {1} The {0}".format("Office", "love")
>>> txt
'I love The Office'
```
10. format_map 
```python
>>> kv = {'a' : 'Python', 'b': 'like'}
>>> x = 'I {b} {a}'.format_map(kv)
>>> x
'I like Python'
```
11. Index
```python
>>> txt = "Pineapple on Pizza!"
>>> x = txt.index("a")
>>> x
4
```
12. Isalnum
```python
>>> game = "Cyberpunk2077"
>>> x = game.isalnum()
>>> x
True
``` 
13. Isapha
```python
>>> name = "Andy123"
>>> is_alpha = name.isalpha()
>>> is_alpha
False
``` 
14. Isascii 
```python
>>> game = "Cyberpunk2022"
>>> is_ascii = game.isascii()
>>> is_ascii
True
```
15. Isdecimal
```python
>>> txt = "\u0033"
>>> x = txt.isdecimal()
>>> x
True
``` 
16. Isdigit
```python
value = "5000"
>>> is_digit = value.isdigit()
>>> is_digit
True
``` 
17. Isidentiifier
```python
>>> txt = "2022Cyber"
>>> x = txt.isidentifier()
>>> x
False
``` 
18. Isnumeric
```python
>>> txt = "2022"
>>> x = txt.isnumeric()
>>> x
True
``` 
19. Isprintable 
```python
>>> txt = 'Hey\nMy name is Tenzin'
>>> x = txt.isprintable()
>>> x
False
```
20. Islower
```python
>>> name = "tenzin"
>>> is_lower = name.islower()
>>> is_lower
True
``` 
21. Isspace
```python
>>> txt = "   "
>>> x = txt.isspace()
>>> x
True
``` 
22. Isupper
```python
>>> txt = "THIS IS THE TEXT"
>>> x = txt.isupper()
>>> x
True
``` 
23. Istitle
```python
>>> txt = "I Like Tech Twitter"
>>> x = txt.istitle()
>>> x
True
``` 
24. Join
```python
>>> morning = {"shower", "breackfast", "work"}
>>> morning_join = " > ".join(morning)
>>> morning_join
'work > shower > breackfast'
```
25. ljust
```python
>>> txt = "JaveScript"
>>> x = txt.ljust(20, ".")
>>> x
'JaveScript..........'
```
26. Lower
```python
>>> name = "Tenzin Tsundue"
>>> lower_name = name.lower()
>>> lower_name
'tenzin tsundue'
```
27. Istrip 
```python
>>> txt = "     Frodo     "
>>> x = txt.lstrip()
>>> print("Hello", x, "!")
Hello Frodo      !
```
28. Maketrans
```python
>>> txt = "Harry Cotter"
>>> tbl = txt.maketrans("C", "P")
>>> print(txt.translate(tbl))
Harry Potter
``` 
29. Partition
```python
>>> txt = "HTML is a programming language?"
>>> x = txt.partition('programming')
>>> x
('HTML is a ', 'programming', ' language?')
```
30. Replace
```python
>>> txt = "That's a red wine"
>>> txt2 = txt.replace("red", "white")
>>> txt2
"That's a white wine"
``` 
31. Rfind
```python
>>> txt = "I love coffee coffee"
>>> x = txt.rfind("coffee")
>>> x
14
```
32. Rindex
```python
>>> txt = "I love coffee coffee"
>>> x = txt.rindex("coffee")
>>> x
14
``` 
33. Rjust
```python
>>> txt = "JaveScript"
>>> x = txt.rjust(20, ".")
>>> x
'..........JaveScript'
```
34. Rpartition
```python
>>> txt = "One for you and one for me."
>>> x = txt.rpartition("for")
>>> x
('One for you and one ', 'for', ' me.')
``` 
35. Rsplit
```python
>>> txt = "No! No! No! No! No!"
>>> x = txt.rsplit("! ", 3)
>>> x
['No! No', 'No', 'No', 'No!']
```
36. rstrip
```python
>>> x = txt.rstrip()
>>> print("Hello", x, "!")
Hello      Frodo !
```
37. split
```python
>>> txt = "No! No! No! No! No!"
>>> x = txt.split("! ", 3)
>>> x
['No', 'No', 'No', 'No! No!']
```
38. splitlines
```python
>>> txt = "hey there\nHow's your day going?"
>>> x = txt.splitlines(True)
>>> x
['hey there\n', "How's your day going?"]
```
39. startswith
```python
>>> name = "Tenzin"
>>> start = name.startswith("Mi")
>>> start
False
```
40. strip
```python
>>> txt = "    Tenzin    "
>>> x = txt.strip()
>>> print("Hello", x, "!")
Hello Tenzin !
```
41. swapcase
```python
>>> txt = "e.t. PHONE HOME"
>>> x = txt.swapcase()
>>> x
'E.T. phone home'
```
42. title
```python
>>> txt = "This is my place"
>>> x = txt.title()
>>> x
'This Is My Place'
```
43. translate
```python
>>> dict_ascii = {74 : 80, 105 : 97}
>>> txt = "Jim".translate(dict_ascii)
>>> txt
'Pam'
```
44. upper
```python
>>> names = "JIm aNd DwIGht"
>>> upper_names = names.upper()
>>> upper_names
'JIM AND DWIGHT'
```
45. zfill
```python
>>> price  = ".125"
>>> price_fill = price.zfill(6)
>>> price_fill
'00.125'
```
46. remobeprefix
```python
>>> name = "Aaron"
>>> name_new = name.removeprefix("Aar")
>>> name_new
on
```
47. removesuffix
```python
>>> name = "Aaron"
>>> name_new = name.removesuffix("on")
>>> name_new
Aaron
```
