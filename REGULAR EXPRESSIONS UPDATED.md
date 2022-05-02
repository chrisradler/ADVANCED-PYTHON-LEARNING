```python
text = "The agents phone number is 408-555-1234. Call soon!"

```


```python
'phone' in text
```




    True




```python
import re
```


```python
pattern = 'phone'
```


```python
re.search(pattern,text)
```




    <re.Match object; span=(11, 16), match='phone'>




```python
pattern = 'NOT IN TEXT'
```


```python
re.search(pattern,text)
```


```python
pattern = 'phone'
```


```python
match = re.search(pattern,text)
```


```python
match
```




    <re.Match object; span=(11, 16), match='phone'>




```python
match.span()
```




    (11, 16)




```python
match.start()
```




    11




```python
match.end
```




    <function Match.end(group=0, /)>




```python
text = 'my phone once, my phone twice'
```


```python
match = re.search('phone',text)
```


```python
match
```




    <re.Match object; span=(3, 8), match='phone'>




```python
matches = re.findall('phone',text)
```


```python
matches
```




    ['phone', 'phone']




```python
len(matches)
```




    2




```python
for match in re.finditer('phone',text):
    print(match)
```

    <re.Match object; span=(3, 8), match='phone'>
    <re.Match object; span=(18, 23), match='phone'>



```python
text = 'My phone number is 408-555-7777'
```


```python
phone = re.search('\d\d\d-\d\d\d-\d\d\d\d',text)
```


```python
phone
```




    <re.Match object; span=(19, 31), match='408-555-7777'>




```python
phone.group
```




    <function Match.group>




```python

```


```python
phone = re.search('\d{3}-\d{3}-\d{4}',text)
```


```python
phone
```




    <re.Match object; span=(19, 31), match='408-555-7777'>




```python
phone_pattern = re.compile('(\d{3})-(\d{3})-(\d{4})')
```


```python
phone_pattern
```




    re.compile(r'(\d{3})-(\d{3})-(\d{4})', re.UNICODE)




```python
results = re.search(phone_pattern,text)
```


```python
results.group()
```




    '408-555-7777'




```python
results.group(1)
```




    '408'




```python
re.search(r'cat|dog','The dog is here')
```




    <re.Match object; span=(4, 7), match='dog'>




```python
re.findall(r'.at','The cat in the hat sat there.')
```




    ['cat', 'hat', 'sat']




```python
 re.findall(r'^\d','1 is a number')
```




    ['1']




```python

```


```python

```


```python

```


```python

```


```python
phrase = 'there are 3 numbers 34 inside 5 this sentence'
```


```python
pattern = r'[^\d]'
```


```python
re.findall(pattern,phrase)
```




    ['t',
     'h',
     'e',
     'r',
     'e',
     ' ',
     'a',
     'r',
     'e',
     ' ',
     ' ',
     'n',
     'u',
     'm',
     'b',
     'e',
     'r',
     's',
     ' ',
     ' ',
     'i',
     'n',
     's',
     'i',
     'd',
     'e',
     ' ',
     ' ',
     't',
     'h',
     'i',
     's',
     ' ',
     's',
     'e',
     'n',
     't',
     'e',
     'n',
     'c',
     'e']




```python
test_phrase = 'This is a string! But it has punctuation. How can we remove it?'
```


```python
clean = re.findall(r'[^!.?]+',test_phrase)
```


```python
clean = re.findall
```


```python

```


```python

```
