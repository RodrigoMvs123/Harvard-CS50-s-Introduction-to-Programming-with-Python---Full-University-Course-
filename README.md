# Harvard-CS50-s-Introduction-to-Programming-with-Python---Full-University-Course-

https://youtu.be/nLRL_NcnK-4

https://raw.githubusercontent.com/RodrigoMvs123/Harvard-CS50-s-Introduction-to-Programming-with-Python---Full-University-Course-/main/README.md

https://github.com/RodrigoMvs123/Harvard-CS50-s-Introduction-to-Programming-with-Python---Full-University-Course-/blame/main/README.md

Modules 

Input
Print 
Print_Column 
Print_Square 
Char
String
Integer 
Float
Boolean
If
Elif
List 
For
Range
While 
While True
Loop
Continue 
Else
Elseif
Break
Define 
Define Main
Get
Get_Int
Prompt
Length
Dictionary 
None
Height 
N/
End=""
Sep=""
Row
Width
Size
Try
Except 
NameError
ValueError
IndexError
Return
Pass
From
Sys.argv
Sys.exit
Slices
__name__
Assert
AssertionError
Pytest
Open 
With
Csv (Comma separated value)
Regexes 
Strip
Split
Endwith
Re
Tuple
Class
Object
Raise
__str__
@Properties  
Decorators 
Getter
Setter 
@Classmethods
@Staticmethod 
Inheritance 
Operator overloading 
Global
Constants 
Type hints 
Mypy
Docstring
Argparse
Unpacking
Map
List comprehension 
Filter 
Dictionary comprehensions 
Enumerate 
Generators 
Yield 
Iterator 
- - - 

Libraries ( Module ) - random
Random.html
docs.python.org/3/library/random.html
Import
random.choice ( sequence )

generate.py
import random

coin = random.choice ( ["heads", "tails"] )
print ( coin )

- - 

generate.py
from random import choice

coin = choice( [ "heads", "tails" ] )
print ( coin )

 - - 

random.randint ( a, b )

generate.py
import random

number = random.randint (1, 10)
print ( number )

- - 

random.shuffle ( x )

generate.py
import random 

cards = [ "jack", "queen", "king" ]
random.shuffle ( cards )
for card in cards:
       print ( card )

- - -

Library - Statistics 
docs.python.org/3/library/statistics.html
average.py 
import statistics 

print ( statistics.mean ( [ 100, 90 ] ) )

- - -

Library - System
docs.python.org/3/library/sys.html
command-line arguments
sys.argv ( argument vector )

name.py
import sys

try
       print ( "hello, my name is", sys.argv [ 1 ] )
except IndexError:
       print ( "too few arguments" )

- -

name.py
import sys

If len ( sys.argv ) < 2:
       print ( "Too few arguments" )
elif len ( sys.argv ) > 2:
       print ( "Too many arguments" )
else 
       print ( "hello, my name is", sys.argv [ 1 ] )

- -

name.py
import sys 

If len ( sys.argv ) < 2:
       sys.exit ( "Too few arguments" )
elif len ( sys.argv ) > 2:
       sys.exit ( "Too many arguments" )
else 

print ( "hello, my name is", sys.argv [ 1 ] )

- -

name.py
import sys 

If len ( sys.argv ) < 2:
       sys.exit ( "Too few arguments" )

for arg in sys.argv [ 1: ]:
print ( "hello, my name is", arg )

"Or 
for arg in sys.argv [ 1: - 1 ]:
print ( "hello, my name is", arg )"

- - -

Packages ( 3rd party libraries )
PYiP.org 
pypi.org/project/cowsay 
Pytest

Cowsay
Package manager ( pip )

Visual Studio Code 
Terminal 
$ pip install cowsay
Successfully installed cowsay-4.0

say.py
import cowsay 
Import sys

if len ( sys.argv ) == 2:
       cowsay.cow ( "hello  " + sys.argv [ 1 ] )

"Or 
if len ( sys.argv ) == 2:
       cowsay.trex ( "hello  " + sys.argv [ 1 ] )
"

- - -

Requests
pypi.org/projects/requests 

Visual Studio Code
Terminal
$ pip install requests 
Successfully installed requests-2.27.1

itunes.py
https://itunes.apple.com/search?entity=song&limit=1&term=weezer 

JSON ( JavaScript Object Notation  ) 

{
 "resultCount":1,
 "results": [
{"wrapperType":"track", "kind":"song", "artistId":115234, "collectionId":1440878798, "trackId":1440879325, "artistName":"Weezer", "collectionName":"Weezer", "trackName":"Buddy Holly", "collectionCensoredName":"Weezer", "trackCensoredName":"Buddy Holly", "artistViewUrl":"https://music.apple.com/us/artist/weezer/115234?uo=4", "collectionViewUrl":"https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4", "trackViewUrl":"https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4", 
"previewUrl":"https://audio-ssl.itunes.apple.com/itunes-assets/AudioPreview112/v4/f0/ba/a8/f0baa81a-7449-c490-f43a-b5c6e3609e3f/mzaf_3988310882581261442.plus.aac.p.m4a", "artworkUrl30":"https://is2-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/30x30bb.jpg", "artworkUrl60":"https://is2-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/60x60bb.jpg", "artworkUrl100":"https://is2-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/100x100bb.jpg", "collectionPrice":9.99, "trackPrice":1.29, "releaseDate":"1994-01-01T12:00:00Z", "collectionExplicitness":"notExplicit", "trackExplicitness":"notExplicit", "discCount":1, "discNumber":1, "trackCount":10, "trackNumber":4, "trackTimeMillis":159587, "country":"USA", "currency":"USD", "primaryGenreName":"Pop", "isStreamable":true}]
}

itunes.py
import requests
import sys 

if len ( sys.argv ) ! = 2:
       sys.exit ( )

response = request.get ( "https://itunes.apple.com/search?entity=song&limit=1&term" + sys.argv [ 1 ] )
print ( response.json ( ) ) 

- - 

docs.python.org/3/library/json.html

itunes.py
import json
import requests
import sys 

if len ( sys.argv ) ! = 2:
       sys.exit ( )

response = request.get ( "https://itunes.apple.com/search?entity=song&limit=1&term" + sys.argv [ 1 ] )

o = response.json ( )
for result in o [ "results" ]:
       print ( result [ "trackName" ] )

- - - 

Libraries 

sayings.py
def main ( ): 
       hello ( "world" )
       goodbye ( "world" )
       
def hello ( name ):
       print ( f "hello, { name}" ) 

def goodbye ( name ):
       print ( f "goodbye, { name}" )

If __name__ == "__main__":
       main ( )

- - 

say.py
import sys

from sayings import hello 

if len ( sys.argv ) == 2:
       print ( sys.argv [ 1 ] ) 

- - - 

Unit Tests 

Pytest
Docs.pytest.org
Pip install pytest

calculator.py
def main ( ):
       x = int ( input ( "Whats is x ? " ) ) 
       print ( " x square is ", square ( x ) )

def square ( n ):
       return n * n 

if __name__ == " __main__ ":
       main (  )

- - 

test_calculator.py
from calculator import square

def main ( )
       test_square ( )

def test_square (  ):
       try:
              assert square ( 2 ) == 4
       except AssertionError: 
              print ( " 2 square was not 4 " ) 
       try:
              assert square ( 3 ) == 9
       except AssertionError: 
              print ( " 3 square was not 9 " )
      try:
              assert square ( -2 ) == 4
       except AssertionError: 
              print ( " -2 square was not 4 " ) 
       try:
              assert square ( -3 ) == 4
       except AssertionError: 
              print ( " -3 square was not 4 " ) 
       try:
              assert square ( 0 ) == 0
       except AssertionError: 
              print ( " 0 square was not 0 " ) 

if __name__ == " __main__ ":
       main ( )

- - 

test_calculator.py
from calculator import square 

def test_square ( ):
       assert square ( 2 ) == 4
       assert square ( 3 ) == 9
       assert square ( -2 ) == 4
       assert square ( -3 ) == 9
       assert square ( 0 ) == 0

Visual Studio Code
Terminal
pytest test_calculator.py 

- -

test_calculator.py
import pytest
from calculator import square 

def test_positive ( ):
       assert square ( 2 ) == 4
       assert square ( 3 ) == 9

def test_negative ( ): 
       assert square ( -2 ) == 4
       assert square ( -3 ) == 9

def test_zero ( ):
       assert square ( 0 ) == 0

def test_str ( ):
       with_pytest.raises ( TypeError ) 
              square ( "cat" )

Visual Studio Code
Terminal
pytest test_calculator.py

- - - 

hello.py

def main ( ):
       name = input ( "What is your name " )
       print ( hello ( name ) )

def test_hello ( ):
       return f "hello, { to }"

if __name__ == "__main__":
       main ( )

- - 

test_hello.py
import hello from hello


def test_default ( ):
       assert hello ( "David" ) == " hello, David" )
      
def test_argument ( ):
       for name in [ "Hermione", "Harry", "Ron" ]
              assert hello ( name ) == f"hello, { name }" 

pytest test_hello.py 

- - -

Visual Studio Code
Terminal 
mkdir.test 
code test/test_hello.py 
code /test__init__.py

test_hello.py
from hello import hello 

def test_default ( ):
       assert hello ( ) == "hello, world"

def test_argument ( ):
       assert hello ( "David" ) == "hello, David" 

- - 

__init__.py

- - - 

File I/O ( Input and Output )

List

names.py
name = []

for _ in range ( 3 ) 
       name.append ( input ( "What is your name ?" )
)

for name in sorted ( names ): 
       print ( f " hello,  {name} " )

- -

docs.python.org/3/library/functions.html#open 

names.py
name = input ( " What is your name ? " )

with open ( " names.txt ", "a" ) as file:
       file.write ( f "{ name } \ n " ) 


code names.txt

- - 

names.py

with open ("names.txt", "r") as file:
       lines = file.readlines()

for line in lines: 
       print("hello,", line)
- -

names.py

with open ("names.txt", "r") as file:
       for line in file: 
              print("hello,", line.rstrip() 

- - 

docs.python.org/3/library/functions.html#sorted
sorted(iterable, /, *, key=None, reverse=False)

names.py

names = []

with open = ("names.txt") as file:
       for line in file:
              names.append(line.rstrip())

for name in sorted(names):
       print(f"hello {name}")

- - 

names.py

with open = ("names.txt") as file:
       for line in sorted(file):
              print("hello,", line.rstrip())

- -

names.py

names = []

with open = ("names.txt") as file:
       for line in file:
              names.append(line.rstrip())

for name in sorted(names, reverse=True):
       print(f"hello {name}")

code names.csv (comma separated value)

code students.csv

Hermione, Gryffindor
Harry, Gryffindor
Ron, Gryffindor
Draco, Slytherin 

- - 

code students.py

with open("students.csv") as file:
       for line in file:
              row = line.rstrip().split(",")
              print(f"{row[0]} is in {row[1]})

- - 

code students.py

with open("students.csv") as file:
       for line in file:
              name, house = line.rstrip().split(",")
              print(f"{row[name]} is in {row[house]})

- - 

studentes.py

students = []

with open("students.cvs") as file:
       for line in file:
             name, house = line.rstrip().split(",")
             students.append(f"{name} is in {house}")

for student in sorted(students)
        print(student)

- -

studentes.py

students = []

with open("students.cvs") as file:
       for line in file:
             name, house = line.rstrip().split(",")
             student = {} 
             student ["name"] = name
             student ["house"] = house
             students.append(student)

for student in students: 
       print(f"{student ['name']} is in {student ['house']}")

- - 

studentes.py

students = []

with open("students.cvs") as file:
       for line in file:
             name, house = line.rstrip().split(",")
             student = {"name": name, "house": house} 
             students.append(student)

def get_name(student):
       return student ["name"]

for student in sorted(students, key=get_name):
       print(f"{student ['name']} is in {student ['house']}")

- -

docs.python.or/3/library/csv.html

students.csv

Hermione, Gryffindor
Harry, Gryffindor
Ron, Gryffindor
Draco, Slytherin 

studentes.py
import csv 

students = []

with open("students.cvs") as file:
       reader = csv.reader(file)
       for name, house in reader:
              students.append({"name": name, "house": house}) 

       for student in sorted(students, key=lambda student: student["name"]):
       print(f"{student ['name']} is in {student ['house']}")

- -

students.csv

Hermione, Gryffindor
Harry, Gryffindor
Ron, Gryffindor
Draco, Slytherin 

studentes.py
import csv 

students = []

with open("students.cvs") as file:
       reader = DictReader(file)
       for name, house in reader:
              students.append({"name": row ["name"], "house": row ["house]}) 

       for student in sorted(students, key=lambda student: student["name"]):
       print(f"{student ['name']} is in {student ['house']}")

- - 

students.csv
name, home
Harry, "Number Four, Privet Drive"
Ron, The Burrow
Malfoy, Manor

students.py
import csv

name = input("What is your name ?")
home = input("Where is your home ?")
       
with open("students.csv", "a") as file:
       writer = csv.writer(file)
       write.writerow([name, home])

Visual Studio Code 
Terminal

python students.py 
What is your name ? Harry
Where is your house ? "Number Four, Privet Drive"

Visual Studio Code 
Terminal

python students.py 
What is your name ? Ron
Where is your house ? The Burrow

Visual Studio Code 
Terminal

python students.py 
What is your name ? Draco
Where is your house ? Malfoy Manor

- - 

students.csv
name, home
Harry, "Number Four, Privet Drive"
Ron, The Burrow
Malfoy, Manor

students.py
import csv

name = input("What is your name ?")
home = input("Where is your home ?")
       
with open("students.csv", "a") as file:
       writer = csv.DictWriter(file, fieldnames=["name", "house"])
       write.writerow({"name": name, "home": home}) 

Visual Studio Code 
Terminal

python students.py 
What is your name ? Harry
Where is your house ? "Number Four, Privet Drive"

Visual Studio Code 
Terminal

python students.py 
What is your name ? Ron
Where is your house ? The Burrow

Visual Studio Code 
Terminal

python students.py 
What is your name ? Draco
Where is your house ? Malfoy Manor

- - -

Pil

pillow.readthedocs.io

Visual Studio Code
Terminal
code costume1.gif
codecostume2.gif

code costume.py
import sys

from PIL Import image

images = []

for argv in sys.argv[:1]: 
       image = Image.open(arg)
       Image.append(image)

images[0].save(
       "costumes.gif" save_all=True, append_images= [images [1]], duration=200, 
)

Visual Studio Code 
Terminal 
python costumes.py costume1.gif costume2.gif

code costumes.gif

- - -

Regular Expression for Valid Email Address
(Pattern)
^[a-zA-Z0-9.!#$%&'*+\/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](:?[a-zA-Z0-9]{0,61}[a-zA-Z0-9])?)*$

Regular Expressions 

code validate.py 

validate.py
email = ("What is your email ?).strip() 

if "@" in email: 
       print("Valid")
else
       print("Invalid")

Visual Studio Code 
Terminal
python validate.py
What is your email ? malan@harvard.edu
Valid

python validate.py
What is your email ? @
Valid

- - 

validate.py
email = ("What is your email ?).strip() 

if "@" in email and "." in email: 
       print("Valid")
else
       print("Invalid")

Visual Studio Code 
Terminal
python validate.py
What is your email ? malan@harvard.edu
Valid

python validate.py
What is your email ? @.
Valid

- -

validate.py
email = ("What is your email ?).strip()

username, domain = email.split("@")

if username and "." in domain:
       print("Valid")
else 
       print("Invalid") 

Visual Studio Code 
Terminal
python validate.py
What is your email ? malan@harvard.edu
Valid

python validate.py
What is your email ? malan@harvard
Invalid

- -

validate.py
email = ("What is your email ?).strip()

username, domain = email.split("@")

if username and domain.endwith(".edu"):
       print("Valid")
else 
       print("Invalid")

Visual Studio Code 
Terminal
python validate.py
What is your email ? malan@harvard.edu
Valid

python validate.py
What is your email ? malan@.edu
Invalid

- -

Re
docs.python.org/3/library/re.html
re.search(pattern, string, flags=0)
docs.python.org/3/library/re.html
re.match(pattern, string, flags=0)
docs.python.org/3/library/re.html
re.fullmatch(pattern, string, flags=0)

re.IGNORECASE
re.MULTILINE
re.DOTALL

validate.py
import re

email = ("What is your email ?).strip()

if re.search(r"^\w@(\w+\.)?\w+\.(com|edu|gov|net|org)$", email, re.IGNORECASE):
       print("Valid")
else 
       print("Invalid")

Visual Studio Code 
Terminal
python validate.py
What is your email ? malan@harvard.edu
Valid

python validate.py
What is your email ? @
Valid

python validate.py
What is your email ? malan@harvard?edu
Invalid

python validate.py
What is your email ? malan@
Invalid

python validate.py
What is your email ? My email address is malan@harvard.edu.
Invalid

. any character except a new line
* 0 or more repetitions
+1 or more repetitions 
? 0 or 1 repetition
{m} m repetitions
{m,n} m-n repetitions 
^ matches the start of the string
$ matches the end of the string or just before the new line at the end of the string 
[]set of characters 
[^]complementing the set 
\d decimal digit 
\D not a decimal digit 
\s whitespace character 
\S not a whitespace character 
\w word character… as well as numbers and the underscore 
\W not a word character 
A|B either A or B
(...) a group 
(?:...) non-capturing version 

start -> q1 -> @ -> q2 
start ->  q1 -> q2 -> @ -> q3 -> q4

- - 

code format.py

format.py
name = input("What is your name ?").strip()
       print(f"hello, {name}")

Visual Studio Code
Terminal 
python format.py
What is your name ? David Malan
hello, David Malan

python format.py
What is your name ? Malan, David
hello, Malan, David 

- -

format.py
name = input("What is your name ?").strip()
if "," in name:
       last, first = name.split(", ")
       name = f"{first} {last}"
print(f"hello, {name}")

Visual Studio Code
Terminal 
python format.py
What is your name ? David Malan
hello, David Malan

python format.py
What is your name ? Malan, David
hello, David Malan

python format.py
What is your name ? Malan,David

ValueError: not enough values to unpack (expected 2, got 1)

- - 

format.py
import re

name = input("What is your name ?").strip()
matches = re.search(r"^(.+), (.+)$", name)
if matches:
       last, first = matches.group()
       name = f"{first} {last}"
print("hello, {name}")

Terminal 
python format.py
What is your name ? David Malan
hello, David Malan

python format.py
What is your name ? Malan, David
hello, David Malan

- - 

format.py
import re

name = input("What is your name ?").strip()
matches = re.search(r"^(.+), (.+)$", name)
if matches:
       last = matches.group(1)
       name = matches.group(2)
       name = f"{first} {last}"
print("hello, {name}")

- - 

format.py
import re

name = input("What is your name ?").strip()
matches = re.search(r"^(.+), *(.+)$", name)
if matches:
       name = matches.group(2) + " " + matches.group(1)
print("hello, {name}")

Terminal 
python format.py
What is your name ? David Malan
hello, David Malan

python format.py
What is your name ? Malan, David
hello, David Malan

python format.py
What is your name ? Malan,David
hello, David Malan

python format.py
What is your name ? Malan,      David
hello, David Malan

- - 

format.py
import re

name = input("What is your name ?").strip()
if matches := re.search(r"^(.+), *(.+)$", name):
       name = matches.group(2) + " " + matches.group(1)
print("hello, {name}")

Visual Studio Code
Terminal
python format.py
What is your name ? Malan,David
hello, David Malan

- - - 

code twitter.py

twitter.py
url = input("URL: ").strip()
print(url)

Visual Studio Code 
Terminal
python twitter.py
URL: https://twitter.com/davidjmalan
https://twitter.com/davidjmalan

- -

twitter.py
url = input("URL: ").strip()

username = url.replace("https://twitter.com/", "")
print(f"Username: {username}")

Visual Studio Code 
Terminal
python twitter.py
URL: https://twitter.com/davidjmalan
Username: davidjmalan 

- -

Re

docs.python.org/3/library/re.html
re.sub(pattern, repl, string, count=0, flags=0)
re.split(pattern, string, maxsplit=0, flags=0)
re.findall(pattern, string, flags=0)

twitter.py
url = input("URL: ").strip()

username = url.removeprefix("https://twitter.com/", "")
print(f"Username: {username}")

Visual Studio Code 
Terminal
python twitter.py
URL: My username is https://twitter.com/davidjmalan
Username: My username is https://twitter.com/davidjmalan

- - 

twitter.py
import re

url = input("URL: ").strip()

username = re.sub(r"^(https?://)?(www\.)witter\.com/", "", url)
print(f"Username: {username}")

Visual Studio Code 
Terminal
python twitter.py
URL: https://twitter.com/davidjmalan
Username: davidjmalan 

- -

twitter.py
import re

url = input("URL: ").strip()

if matches := re.search(r"^https?://(?:www\.)?twitter\.com/([a-z0-9_]+)", url, re.IGNORECASE):
       print(f"Username:", matches.group(1))

Visual Studio Code 
Terminal
python twitter.py
URL: https://twitter.com/davidjmalan
Username: davidjmalan 

Object-Oriented Programming

code student.py

student.py 
name = input("Name: ")
house = input("House: ")
print(f"{name} from {house}")

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor 

- - 

student.py 
def main():
       name = get_name()
       house = get_house()
       print(f"{name} from {house}")


def get_name():
       return input("Name: ")
       
def get_house():
       return input("House: ")

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor 

- - 

student.py 
def main():
       student = get_student()
       if student[0] == "Padma":
              student[1] = "Ravenclaw"
       print(f"{student[0]} from {student[1]}")

 def get_student 
       name = input("Name: ")
       house = input("House: ")
       return [name, house]

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Padma
House: Gryffindor
Padma from Ravenclaw
 
- - 

student.py 
def main():
       student = get_student()
       if student ["name"] == "Padma"
              student ["house"] = "Ravenclaw" 
       print(f"{student['name']} from {student['house']}")

 def get_student 
       student = {}
       name = input("Name: ")
       house = input("House: ")
       return {"name": name, "house: house"}

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor

python student.py
Name: Padma
House: Gryffindor
Padma from Ravenclaw

- -

docs.python.org/3/tutorial/classes.html

student.py 
class Student

def main():
       student = get_student()
       print(f"{student.'name} from {student.house}")

 def get_student 
       student = Student()
       student.name = input("Name: ")
       student.house = input("House: ")
       return student 

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor

- -

student.py 
class Student:
       def __init__ (self, name, house): 
              if not name: 
                     raise ValueError("Missing name")
             if house not in ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slitherin"]:
                     raise ValueError("Invalid house")
              self.name = name
              self.house = house 

def main():
       student = get_student()
       print(f"{student.'name} from {student.house}")

 def get_student 
       student = Student()
       name = input("Name: ")
       house = input("House: ")
       return Student(name, house) 
      

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor

- - 

student.py 
class Student:
       def __init__ (self, name, house, patronus): 
              if not name: 
                     raise ValueError("Missing name")
             if house not in ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slitherin"]:
                     raise ValueError("Invalid house")
              self.name = name
              self.house = house 
              self.patronus = patronus

       def __str__ (self)
              return f"{self.name} from {self.house}

def charm(self)
       match self.patronus: 
              case "Stag": 
                     return "horse emoji" 
              case "Otter": 
                     return "...emoji"
              case "Jack Russell terrier":
                     return "dog emoji"
              case "_: 
                     return "/"

def main():
       student = get.student()
       print("Expecto Patronum !") 
       print(student.charm())
       
def get_student 
       student = Student()
       name = input("Name: ")
       house = input("House: ")
       patronus = input("Patronus: ")
       return Student(name, house, patronus) 

if __name__ == "__main__":
       main()


Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Patronus: Stag
Expecto Patronum !
horse emoji 

python student.py
Name: Draco
House: Slytherin 
Patronus: 
Expecto Patronum !
/

- -

student.py 
class Student:
       def __init__ (self, name, house): 
              if not name: 
                     raise ValueError("Missing name")
             if house not in ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slitherin"]:
                     raise ValueError("Invalid house")
              self.name = name
              self.house = house 
              
       def __str__ (self)
              return f"{self.name} from {self.house}

def main():
       student = get.student()
       student.house = "Number Four, Privet Drive"
       print(student) 
              
def get_student 
       student = Student()
       name = input("Name: ")
       house = input("House: ")
       return Student(name, house) 

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Number Four, Privet Drive

- - 

student.py 
class Student:
       def __init__ (self, name, house): 
              self.name = name
              self.house = house 
              
       def __str__ (self)
              return f"{self.name} from {self.house}

       @property
       def name(self):
              return self._name 

       @name.setter 
       def name(self, name)
              if not name:
                     raise ValueError("Missing name") 
              self._name = name

# Getter 
       @property
       def house(self): 
       return self._house 

# Setter
      @house.setter 
def house(self, house):
       if house not in["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]:
              raise ValueError("Invalid house")
       self._house = house 

def main():
       student = get.student()
       student._house = "Number Four, Privet Drive"
       print(student) 
              
def get_student 
       student = Student()
       name = input("Name: ")
       house = input("House: ")
       return Student(name, house) 

if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Number Four, Privet Drive 

- - -

code type.py

type.py
print(type(50))

Visual Studio Code
Terminal
python type.py
<class 'int'>

- -


type.py
print(type("hello, world !)")

Visual Studio Code
Terminal
python type.py
<class 'str'>

- - 

type.py
print(type([]))

Visual Studio Code
Terminal
python type.py
<class 'list'>

- -

type.py
print(type(list()))

Visual Studio Code
Terminal
python type.py
<class 'list'>


- -

type.py
print(type({}))

Visual Studio Code
Terminal
python type.py
<class 'dict'>

- -

type.py
print(type(dict()))

Visual Studio Code
Terminal
python type.py
<class 'dict'>

- - - 

code hat.py

hat.py
class Hat:
       def sort(self, name):
               print(name, "is in, "some house")

hat = Hat()
hat.sort("Harry")

Visual Studio Code
Terminal
python hat.py
Harry is in some house

- -

hat.py
import random

class Hat:
       def __init__ (self):
               self.houses["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]

               def sort(self, name):
                      print(name, "is in, random.choises(self, houses)
)

hat = Hat()
hat.sort("Harry")

Visual Studio Code
Terminal
python hat.py
Harry is in Hufflepuff 

Visual Studio Code
Terminal
python hat.py
Harry is in Ravenclaw 


- -

hat.py
import random

class Hat:
       houses["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]

       @classmethod
       def sort(cls, name):
                      print(name, "is in, random.choises(cls, houses)
)

Hat.sort("Harry")

Visual Studio Code
Terminal
python hat.py
Harry is in Hufflepuff 

Visual Studio Code
Terminal
python hat.py
Harry is in Gryffindor 

- - - 

student.py 
class Student:
       def __init__ (self, name, house): 
              self.name = name
              self.house = house 
              
       def __str__ (self)
              return f"{self.name} from {self.house}

       @classmethod
       def get(cls):
              name = input("Name: ")
              house = input("House: ")
              return cls(name, house) 

def main():
       student = Student.get()
       print(student) 
              
if __name__ == "__main__":
       main()

Visual Studio Code 
Terminal 
python student.py
Name: Harry
House: Gryffindor
Harry from Gryffindor 

- - -

docs.python.org/3/library/exeptions.html 
BaseException
 +-- KeyboardInterrupt 
 +-- Exception  
       +-- ArithmeticError 
       |    +-- ZeroDivisionError
       +-- AssertionError 
       +-- AttributeError
       +-- EOFError
       +-- ImportError
       |    +-- ModuleNotFoundError
       +-- LookupError
       |     +-- KeyError
       +-- NameError
       +-- SyntaxError
       |     +-- IdentationError
       +-- ValueError
…
       


code wizard.py

wizard.py
class Wizard:
       def __init__(self, name):
              if not name:
                     raise ValueError("Missing name")
              self.name = name

class Student(Wizard):
       def __init__(self, name, house):  
              super().__init__(name)
              self.house = house 

class Professor(Wizard): 
        def __init__(self, name, subject):
              super().__init__(name)
              self.subject = subject 

wizard = Wizard("Albus") 
student = Student("Harry", "Gryffindor")
professor = Professor("Severus", "Defense Against the Dark Arts") 

- - - 

code vault.py

vault.py
class Vault:
       def __init__(self, galleons=0, sickles=0, knuts=0):
              self.galleons = galleons 
              self.sickles = sickles 
              self.knuts = knuts 

       def __str__(self):
              return f"{self.galleons} Galleons, {self.sickles} Sickles, {self.knuts} Knuts"

potter = Vault(100, 50, 25)
print(potter)

Visual Studio Code 
Terminal
python vault.py
100 Galleons, 50 Sickles, 25 Knuts 

- -

vault.py
class Vault:
       def __init__(self, galleons=0, sickles=0, knuts=0):
              self.galleons = galleons 
              self.sickles = sickles 
              self.knuts = knuts 

       def __str__(self):
              return f"{self.galleons} Galleons, {self.sickles} Sickles, {self.knuts} Knuts"

potter = Vault(100, 50, 25)
print(potter)

weasley = Vault(25, 50, 100)  
print(weasley) 

Visual Studio Code 
Terminal
python vault.py
100 Galleons, 50 Sickles, 25 Knuts 
25 Galleons, 50 Sickles, 100 Knuts

- - 

vault.py
class Vault:
       def __init__(self, galleons=0, sickles=0, knuts=0):
              self.galleons = galleons 
              self.sickles = sickles 
              self.knuts = knuts 

       def __str__(self):
              return f"{self.galleons} Galleons, {self.sickles} Sickles, {self.knuts} Knuts"

potter = Vault(100, 50, 25)
print(potter)

weasley = Vault(25, 50, 100)  
print(weasley) 

galleons = potter.galleons + weasley.galleons 
sickles = potter.sickles + waesley.sickles
Knuts = potter.knuts + weasley.knuts 

total = Vault(galleons, sickles, knuts)
print(total) 

Visual Studio Code 
Terminal
python vault.py
100 Galleons, 50 Sickles, 25 Knuts 
25 Galleons, 50 Sickles, 100 Knuts
125 Galleons, 100 Sickles, 125 Knuts

- - 

docs.python.org/3/reference/datamodel.html#special-method-names
object.__add__(self, other) 

vault.py
class Vault:
       def __init__(self, galleons=0, sickles=0, knuts=0):
              self.galleons = galleons 
              self.sickles = sickles 
              self.knuts = knuts 

       def __str__(self):
              return f"{self.galleons} Galleons, {self.sickles} Sickles, {self.knuts} Knuts"

        def.__add__(self, other):
               galleons = self.galleons + other.galleons
               sickles = self.sickles + other.sickles
               knuts = self.knuts + other.knuts
               return Vault(galleons, sickles, knuts) 
 
potter = Vault(100, 50, 25)
print(potter)

weasley = Vault(25, 50, 100)  
print(weasley) 

total = potter + weasley 
print(total) 

Visual Studio Code 
Terminal
python vault.py
100 Galleons, 50 Sickles, 25 Knuts 
25 Galleons, 50 Sickles, 100 Knuts
125 Galleons, 100 Sickles, 125 Knuts

- - -

Et Cetera 

code houses.py 

houses.py
students = [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
       {"name": "Padma", "house": "Ravenclaw"},
]

houses = []
for student in students: 
       if student["house"] not in houses:
              houses.append(student["house"])

for house in sorted(houses):
       print(house)

Visual Studio Code
Terminal
python houses.py
Gryffindor
Ravenclaw
Slytherin 

- - 

houses.py
students = [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
       {"name": "Padma", "house": "Ravenclaw"},
]

houses = set()
for student in students: 
       houses.add(student["house"])

for house in sorted(houses):
       print(house)

Visual Studio Code
Terminal
python houses.py
Gryffindor
Ravenclaw
Slytherin 

- - -

code bank.py

bank.py
balance = 0

def main():
       print("Balance":, balance)
       deposit(100)
       withdraw(50) 
       print("Balance":, balance)

def deposit(n):
       global balance
       balance += n

def withdraw(n):
       global balance 
       balance -= n

if __name__  == "__main__":
       main()

Visual Studio Code
Terminal
python bank.py
Balance: 0
Balance: 50

- -

bank.py
class Account:
       def __init__ (self): 
              self._balance = 0

       @property 
       def balance(self):
              return self.balance 

        def deposit(self, n): 
               self._balance += n 

        def withdraw(self, n): 
               self._balance -= n 

def main():
         account = Account()
         print("Balance":, account.balance) 
         account.deposit(100) 
         account.withdarw(50) 
         print("Balance":, account.balance)

if __name__ == "__init__": 
         main() 

Visual Studio Code
Terminal
python bank.py
Balance: 0
Balance: 50

- - - 
code meows.py

meows.py
MEOWS = 3

for _ in range(MEOWS):
       print("meow")

- -

meows.py
Class Cat:
       MEOWS = 3

       def meow(self): 
              for _ in range(Cat.MEOWS): 
                     print("meow") 

cat = Cat()
cat.meow()

Visual Studio Code
Terminal 
python meows.py
meow
meow
meow

- - 

docs.python.org/3/library/typing.html 
pip install mypy ( mypy.readthedocs.io )

meows.py
def meow(n: int):
       for _ in rang(n):
              print("meow") 

number: int = int (input("Number: "))
meow(number) 

Visual Studio Code 
Terminal 
mypy meows.py
Success: no issues found in 1 source file 

python meows.py
Number : 3
meow
meow
meow

- -

meows.py
def meow(n: int) -> str:
       return "meow/n" * n 

number: int = int (input("Number: "))
meows: str = meow(number) 
print(meows, end="") 

Visual Studio Code
Terminal 
python meows.py 
Number: 3 
meow
meow
meow

- - 

peps.pythpn.prg/pet-0257/ 

meows.py
def meow(n: int) -> str:
       """Meow n times."""
       return "meow/n" * n 

number: int = int (input("Number: "))
meows: str = meow(number) 
print(meows, end="") 

- - 

meows.py
def meow(n: int) -> str:
       """
       Meow n times.

       :param n: Number of times to meow
       :type n: int
       : raise TypeError: If n is not an int
       :return: A string of meows, one per line
       :rtype: str
       """
       return "meow/n" * n 

number: int = int (input("Number: "))
meows: str = meow(number) 
print(meows, end="") 

- -

meows.py
import sys

if len(sys.argv) == 1:
       print("meow") 
elif len(sys.argv) == 3 and sys.argv[1] == "-n":
       n = int(sys.argv[2])
       for _ in range(n):
              print("meow")
else:
       print("usage: meows.py") 

Visual Studio Code 
Terminal 
python meows.py -n 3
meow
meow
meow
python meows.py -n 2
meow
meow
python meows.py -n 1
meow
python meows.py 
meow

- - 

docs.python.org/3/library/argparse.html

meows.py
import argparse

parser = argparse.Argument.Parser(description"Meow like a cat")
parser.add_argument("-n", default=1, help="number of times to meow", type=int)
args = parser.parse_args()

for _ in range(args.n):
       print("meow") 

Visual Studio Code 
Terminal 
python meows.py 
meow

- - -

code unpack.py

unpack.py
first, _ = input("What is your name?").split(" ")
print(f"Hello, {first}")

Visual Studio Code
Terminal
python unpack.py
What is your name? David Malan
Hello, David 

- -

unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

print(total(100, 50, 25), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- - 

unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

coins[100, 50, 25]

print(total(coins[0], coins[1], coins[2]), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- -

unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

coins[100, 50, 25]

print(total(*coins), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- -

unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

print(total(galleons=100, sickles=50, knutd=25), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- -


unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

coins {"galleons": 100, "sickles": 50, "knuts": 25}

print(total(coins["galleons"], cois["sickles"], coins["knuts"]), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- -

unpack.py
def total(galleos, sickles, knuts):
       return(galleons * 17 * sickles) * 29 + knuts

coins {"galleons": 100, "sickles": 50, "knuts": 25}

print(total(**coins), "Knuts")

Visual Studio Code
Terminal
python unpack.js 
50775 Knuts

- - 

*args, **kwargs 

unpack.py
def f(*args, **kwargs):
       print("Positional:", args)

f(100, 50, 25, 5)

Visual Studio Code
Terminal
python unpack.py
Positional: (100, 50, 25, 5)

- -

unpack.py
def f(*args, **kwargs):
       print("Namedl:", kwargs)

f(galleons=100, sickles=50, knuts=25)

Visual Studio Code
Terminal
python unpack.py
Named: {"galleons": 100, "sickles": 50, "knuts": 25}

- -

docs.python.org/3/library/functions.html#print
print(*objects, sep=' ', end='/n', file=sys.stdout, flush=false)

unpack.py
def print(*objects, sep=" ", end="/n", …):
       for object in objects: 
              … 

- - -

code yell.py

yell.py
def main():
       yell("This is CS50")

del yell(phrase): 
       print(phrase.upper())

if __name__ == "__main__":
       main()

Visual Studio Code
Terminal
python yell.py
THIS IS CS50

- -

yell.py
def main():
       yell(["This", "is", "CS50"])

del yell(word): 
       uppercased = []
              for word in words:
             uppercased.append(word.upper())
       print(*uppercased)

if __name__ == "__main__":
       main()

Visual Studio Code
Terminal
python yell.py
This is CS50

- -


yell.py
def main():
       yell("This", "is", "CS50")

del yell(*words): 
       uppercased = []
              for word in words:
             uppercased.append(word.upper())
       print(*uppercased)

if __name__ == "__main__":
       main()

Visual Studio Code
Terminal
python yell.py
This is CS50

- -

docs.python.org/3/library/functions.html#map 
            map(function, iterable, …)


yell.py
def main():
       yell("This", "is", "CS50")

del yell(*words): 
        uppercased = map(str.upper, words)
        print(*uppercased)

if __name__ == "__main__":
       main()

Visual Studio Code
Terminal
python yell.py
This is CS50

- -

yell.py
def main():
       yell("This", "is", "CS50")

del yell(*words): 
        uppercased = [word.upper() for word in words]
        print(*uppercased)

if __name__ == "__main__":
       main()

Visual Studio Code
Terminal
python yell.py
This is CS50

- - - 

code gryffindof.py

gryffindor.py
students= [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
 ]

gryffindors = [
       student ["name"] for student in students if student ["house"] == "Gryffindor"
]

for gryffindor in sorted(gryffindors):
       print(gryffindor) 

Visual Studio Code
Terminal 
python gryffindor.py
Harry
Hermione
Ron 

- -

docs.python.org/3/library/functions.html#filter
            filter(function, iterable)

gryffindor.py
students= [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
 ]

def is_gryffindor(s)
       return s["house"] == "Gryffindor"

gryffindors = filter(is_gryffindor, students)

for gryffindor in gryffindors:
        print(gryffindor ["name"]) 

Visual Studio Code 
Terminal 
python gryffindor.py
Hermione 
Harry
Ron 

- -


gryffindor.py
students= [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
 ]

def is_gryffindor(s)
       return s["house"] == "Gryffindor"

gryffindors = filter(is_gryffindor, students)

for gryffindor in sorted(gryffindors, key=lambda s: s["name"])
        print(gryffindor ["name"]) 

Visual Studio Code 
Terminal 
python gryffindor.py
Harry
Hermione 
Ron 

- -

gryffindor.py
students= [
       {"name": "Hermione", "house": "Gryffindor"},
       {"name": "Harry", "house": "Gryffindor"},
       {"name": "Ron", "house": "Gryffindor"},
       {"name": "Draco", "house": "Slytherin"},
 ]

gryffindors = filter(lambda s: s["name"] == Gryffindor, students)

for gryffindor in gryffindors:
        print(gryffindor ["name"]) 

Visual Studio Code 
Terminal 
python gryffindor.py
Hermione 
Harry
Ron 

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

gryffindor = []

for student in students: 
       gryffindor.append({"name": student, "house": Gryffindor})

print(gryffindors) 

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

gryffindors = [{"name": student, "house": "Gryffindor"} for student in students]

print(gryffindors)

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

gryffindor = {student: "Gryffindor" for student in students} 

print(gryffindors) 

Visual Studio Code
Terminal
python gryffindor.py
{'Hermione': 'Gryffindor', 'Harry': 'Gryffindor', 'Ron': 'Gryffindor'}

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

for student in students:
       print(students)

Visual Studio Code
Terminal
python gryffindor.py
Hermione
Harry
Ron

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

for i in range(len(students))
       print(i, students[i]])

Visual Studio Code
Terminal
python gryffindor.py
0 hermione
1 harry
2 ron

- -

gryffindor.py
students = ["hermione", "harry", "ron"]

for i in range(len(students))
       print(i + 1, students[i]])

Visual Studio Code
Terminal
python gryffindor.py
1 hermione
2 harry
3 ron

- -

docs.python.org/3/library/functions.html#enumerate
            enumerate (iterable, start=0)

gryffindor.py
students = ["hermione", "harry", "ron"]

for i, student in enumerate(students):
       print(i + 1, student) 

Visual Studio Code
Terminal
python gryffindor.py
1 hermione
2 harry
3 ron

- - -

code sleep.py 

sleep.py
n = int(input("What is n ?))
for i in range(n):
       print("🚢" * i)

Visual Studio Code
Terminal
python sleep.py
What is n ? 4
🚢
🚢🚢
🚢🚢🚢
🚢🚢🚢🚢

- -

sleep.py
def main()
       n = int(input("What is n ?))
       for i in range(n):
              print("🚢" * i)

if __name__ == "__main__":
       main() 

Visual Studio Code
Terminal
python sleep.py
What is n ? 4
🚢
🚢🚢
🚢🚢🚢
🚢🚢🚢🚢

- - 

sleep.py
n = int(input("What is n ?))
for i in range(n):
       print(sheep [i])

def sheep(n):
       return "🚢" * n

if __name__ == "__main__":
       main() 

Visual Studio Code
Terminal
python sleep.py
What is n ? 4
🚢
🚢🚢
🚢🚢🚢
🚢🚢🚢🚢

- -

docs.python.org/3/howto/functional.html#generators
Yield

sleep.py
def main():
       n = int(input("What is n ?))
       for f in sheep(n):        
              print(s)

def sheep(n):
       for i in range (n):
              yield "🚢" * i

if __name__ == "__main__":
       main() 

Visual Studio Code
Terminal
python sleep.py
What is n ? 4
🚢
🚢🚢
🚢🚢🚢
🚢🚢🚢🚢

- - -

code say.py

say.py
import cowsay
import pyttsx3 

engine = pyttsx3.init()
this = input("What is this ?")
cowsay.cow(this)
engine.say(this)
engine.runAndSay()

Visual Studio Code 
Terminal
What is this ? This was CS50

This was CS50
                       ^   ^
                       O  O
                              | - - - - - - |~ 
                                  |       |
                       -      - 

