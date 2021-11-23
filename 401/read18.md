# Automation
## Python Regular Expression Tutorial

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. 

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:

```
import re
```
## Basic Patterns: Ordinary Characters

You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

Examples are 'A', 'a', 'X', '5'.

Ordinary characters can be used to perform simple exact matches:

```
attern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
Match!
```

## Wild Card Characters: Special Characters
* $ - Matches the end of string.
* [abc] - Matches a or b or c.
* [a-zA-Z0-9] - Matches any letter from (a to z) or (A to Z) or (0 to 9).
* \ - Backslash.
Perhaps, the most diverse metacharacter!!
* \w - Lowercase 'w'. Matches any single letter, digit, or underscore.
* \W - Uppercase 'W'. Matches any character not part of \w (lowercase w).
* \s - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
* \S - Uppercase 'S'. Matches any character not part of \s (lowercase s).
* \d - Lowercase d. Matches decimal digit 0-9.
* \D - Uppercase d. Matches any character that is not a decimal digit.
* \t - Lowercase t. Matches tab.
* \n - Lowercase n. Matches newline.
* \r - Lowercase r. Matches return.
* \A - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
* \Z - Uppercase z. Matches only at the end of the string.
* \b - Lowercase b. Matches only the beginning or end of the word.
* {x} - Repeat exactly x number of times.
* {x,} - Repeat at least x times or more.
* {x, y} - Repeat at least x times but no more than y times.

## shutil — High-level File Operations


### Copying Files
```
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))

```
### Working With Directory Trees
```

shutil_copytree.py
import glob
import pprint
import shutil

print('BEFORE:')
pprint.pprint(glob.glob('/tmp/example/*'))

shutil.copytree('../shutil', '/tmp/example')

print('\nAFTER:')
pprint.pprint(glob.glob('/tmp/example/*'))
```
### Finding Files¶
```
import shutil

print(shutil.which('virtualenv'))
print(shutil.which('tox'))
print(shutil.which('no-such-program'))

```
### File System Space
```
shutil_disk_usage.py
import shutil

total_b, used_b, free_b = shutil.disk_usage('.')

gib = 2 ** 30  # GiB == gibibyte
gb = 10 ** 9   # GB == gigabyte

print('Total: {:6.2f} GB  {:6.2f} GiB'.format(
    total_b / gb, total_b / gib))
print('Used : {:6.2f} GB  {:6.2f} GiB'.format(
    used_b / gb, used_b / gib))
print('Free : {:6.2f} GB  {:6.2f} GiB'.format(
    free_b / gb, free_b / gib))
The values returned by disk_usage() are the number of bytes, so the example program converts them to more readable units before printing them.

$ python3 shutil_disk_usage.py

Total: 499.42 GB  465.12 GiB
Used : 246.68 GB  229.73 GiB
Free : 252.48 GB  235.14 GiB
```

