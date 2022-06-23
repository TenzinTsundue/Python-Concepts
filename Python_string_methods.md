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
