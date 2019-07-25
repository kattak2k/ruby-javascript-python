 [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/kattak2k/ruby-javascript-python/issues)
[![HitCount](http://hits.dwyl.io/kattak2k/ruby-javascript-python.svg)](http://hits.dwyl.io/kattak2k/ruby-javascript-python)

# Cheat sheet: Ruby vs Javascript vs Python
An analogy between the Ruby, Javascript and Python languages

### Table Of Contents
1. [Basics Intro](#intro)
2. [Arrays Functions](#functions)
3. [Compound Arrays](#multiple)
4. [String Functions](#strings)
5. [Numerical Functions](#numeric)
6. [Logical Conditions](#conditions)
7. [Class and Methods or Functions](#cmf)
8. [Regular expression (Regex)](#regex)


<h3 id=intro>Basics Intro </h3>

| Description   |Ruby           | Javascript     |Python |
| ------------- |:--------------:| :-----:|:--------:|
| Start Cli| irb | python | node |
| Integers & floats declaration    |``` x = 1 ; y = 0.23 ```|``` let x = 1; var y = 0.23 ```|```x = 1 ; y = 0.23```|
| Contants Declaration     |``` W = 'ruby'.freeze ```|``` const w = 'js' ```|``` W = 'ruby' ```|
| Variables in strings     |``` "one is #{x}" ```|``` `one is ${w}\` ```|``` "one is {}".format(x) ```|
| Line Comment            |``` # this is comment ```|``` // this is comment ```|``` # this is comment ```| 
| Block comments |```=being ;  =end ```|``` /* block comment */ ```|``` ''' block comment ''' ```|
| write output |``` puts 'write output' ```|```console.log('write output')```</br>```document.write("write HTML") ```|```print('write output')```|
| Arrays , Lists    |``` arr = [1,'a',true] ; arr = Array.new ```|```let arr = [1,'a',true]```|``` arr = [1,'a',True] ```|
| Hashes, Objects, dictionaries |```hash = { 'a' => 2, :b => 4 }```|```var obj = { 1 : 2 , 'a' : 4}```|```dict = {1: 2, 'd': 'e' }```|
| Destructuring |``` a,b,c = [2,3,4] ; p b```|``` var {x : a , y: b} = {x : 1, y : 2} ; console.log(b) ```|```a,b,c = [2,3,4]```|


<h3 id=functions>Arrays Functions </h3>
<p><em>where x is [3,4,5,6,7,8]</em></p>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------:| :-----:|:--------:|
| Remove last element|```x.pop```<br/>```x.pop(2)```|```x.pop()```|```x.pop() ```|
| Remove first element|```x.shift(9) ```|```x.shift()```|``` x.remove(x[0])```<br/>```del x[0] ```|
| Add last element|```x.push(9)```<br/>```x.append(9)```<br/>``` x << 9```|```x.push(9)```<br/>```y.concat(5)```|``` x.append(9); x.extend([9]); x.insert(len(x), 9)```|
| Add first element|```x.unshift(2)```|```x.unshift(2)```|``` x.insert(0,2) ```|
| Sort |```x.sort```|```x.sort() ```|```x.sort()```|
| Reverse|```x.reverse```|```x.reverse()```|```x.reverse()```| 
| Count|```x.count(6)```|```var count = {};``` <br/> ```y.forEach(val => count[val] = (count[val] \|\| 0) + 1);```|```x.count(6)```| 
| Length|```x.length; x.size; x.count```|```y.length```|```len(y)```| 
| Maximum|```x.max```|```Math.max(...x)```|```max(x)```| 
| Minimum|```x.min```|```Math.min(...x)```|```min(x)```| 
|index|```x.index(3)```|```x.indexOf(3)```|```x.index(3)```|
|insert|```x.insert(2, 'Feb')```|```x.splice(1, 0, 'Feb')```|```x.insert(2, 'Feb')```|
| Make a copy|```y = x.dup ```|```let y = [...x] ```|``` y = x[:] ```|
| Select, filter |```x.select{\|el\| el > 4 }```|```x.filter((el)=> el > 4)```|```filter(lambda el: el > 4, x)```|
| Reduce |```x.reduce(:+)```|```lx.reduce((result,el)=> result + el,0) ```|```reduce(lambda result,y: result + y, x) ```|
| Map |```x.map{\|el\| el*2}```|```lx.map((el)=> el*2) ```|```map(lambda el: el*2,x)```|
| Each |``` z = []```  </br> ``` x.each{\|el\| z << el*2}``` </br> ```p z ``` |```let z = []``` </br> ```lx.forEach((el) => z.push(el * 2))``` </br> ```console.log(z)```|``` for e in y: ``` </br> ```z.append(e * 2)```</br> ```print z ```|
| Reverse loop |``` z = []```  </br> ``` x.reverse_each{\|el\| z << el*2}``` </br> ```p z ``` |```let z = []``` </br> ```x.slice().reverse().forEach((el) => z.push(el * 2))``` </br> ```console.log(z)```|``` for e in range(len(x) - 1, -1,-1): ``` </br> ```z.append(e * 2)```</br> ```print z ```|
| Clear , Reset |```x.clear```|```x = [] ```|```del x[:]```|

  
<h3 id=multiple>Compound arrays </h3>
<p><em>where, x is [1,2,3] & y is [2,4,5,6]</em></p>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------:| :-----:|:--------:|
|Intersection|```x & y #=> [2]```|```x.filter(e => y.includes(e)) ```|```list(set(x) & set(y)) ```|
|Union|```x \| y```</br>```x.union(y)```|```var z = [...x,...y]```</br>```[...new Set( z )]```</br> 'or'```Array.from(new Set(z)) ```|```list(set(x) \| set(y)) ```|
|Join|```x + y```|```[...x,...y] ```|```x + y```|
|Difference|```x - y```|```x.filter(e => !y.includes(e)); ```|``` list(set(x) - set(y))```|

<h3 id=strings>Strings Functions</h3>
<p><em>where, s = 'Cheat sheet   '</em></p>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------:| :-----:|:--------:|
|UpperCase|```s.upcase```|```s.toUpperCase() ```|```s.upper() ```|
|LowerCase|```s.downcase```|```s.toLowerCase() ```|```s.upper() ```|
|SwapCase|```s.swapcase```|```NA ```|```s.swapcase() ```|
|Trim|```s.strip!```|```s.trim()```|```s.strip() ```|
|StartsWith|```s.start_with?('cheat')```|```s.startsWith('Cheat')```|```s.startswith('Cheat') ```|
|Repeat|```'Hi ' * 3 ```|``` 'Hi '.repeat(3) ```|``` 'Hi ' * 3   ```|
|Split|```'asdf'.split('')```|``` 'asdf'.split('')```|```list('asdf')``` </br>``` 'a#s#d'.split('#')```|
|Join|```['a','s','d','f'].join() ```|```["a", "s", "d", "f"].join('')```|```''.join(['a','s','d'])```|
|Replace|```s.replace('Hey') ```|``` ```|```  ```|
|Find|```  ```|``` ```|```  ```|
|Count|```  ```|``` ```|```  ```|


<h3 id=numeric>Numerical Functions</h3>
<p><em>where, el = -22.45</em></p>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------:| :-----:|:--------:|
|Ceil|```el.ceil ```|``` Math.ceil(el) ```|```import math``` </br>```math.ceil(el) ```|
|Floor|``` el.floor ```|```Math.floor(el)```|```math.floor(el)```|
|Round|``` el.round(1) ```|```Math.round(el)```|```round(el) ```|
|Absolute|``` el.abs ```|```Math.abs(el)```|```abs(el)```|
|Random|``` rand(10) ```|```Math.ceil(Math.random(10) * 11)```|```import random``` </br>```random.randrange(1,10) ```|
|Zero|``` el.zero? ```|``` ```|```  ```|
|Negative|``` el.negative? ```|``` ```|```  ```|


<h3 id=conditions>Logical Conditions</h3>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------| :-----|:--------|
| If |```if <condition1>```</br>```elsif <condition2> ```</br>```else ```</br> ```end```|```if <condition1>:```</br>``` elif <condition2>:```</br> ``` else:```|```if (<condition1>) {```</br>```} else if (<condition2>) {```</br>```} else {```</br>```} ```|  
| case |```case a ```</br>```when <condition1>```</br>```else ```</br> ```end```|```switch(expression) {```</br>```case x:```</br>```break;```</br>```case y:```</br>``` break;```</br>``` default:```</br>```}```|```NA```|  
|Ternary Operator|``` true == false ? 1 : 2 ```|```  true == false ? 1 : 2```|``` 1 if (True == False) else 2```|

<h3 id=cmf>Class and Methods or Functions</h3>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------| :-----|:--------|
|Instance Methods|```def name(input)```</br>``` p input```</br>```end  ```|```name = function(input) {return `${input}`;} ```</br>``` name = (input) => "input"```|```def name(input): ```</br>```print("This is " + input) ```|
|Static Methods|```def self.age(input)```</br>``` p input```</br>```end  ```|```static age(input) {return `${input}`;} ```|```@classmethod ```</br>```def age(input): ```</br>```print("This is " + input) ```|
|Class|```class Person```</br>```attr_accessor :name ```</br>```def initialize(name)```</br>```@name = name```</br>```end```</br>```end```|```class Person {```</br>```constructor(name) {```</br>```this.name = name;```</br>```}```</br>```} ```|```class Person:```</br>```def __init__(self, name):```</br>```self.name = name```|
|create instance Object|```p = Person.new('Bezos')```|```let p = new Person("Bezos")```</br>```let p1 = Object.create(Person)```|```p = Person("Bezos")  ```|
|Single Inheritance |```class Employee < Person```</br>```def initialize(name)```</br>```super name```</br>```@name = name```</br>```end```</br>```end```|```class Employee extends Person {```</br>```constructor(name) {```</br> ``` super(name)```</br>```this.name = name;```</br>```}```</br>```} ```|``` class Employee(Person):```</br>```def __init__(self, name):```</br>```self.name = name```|
|Multiple Inheritance  |```module Student```</br>```def walk```</br>```end```</br>```end ```</br>``` class Person```</br>```include Human```</br>```end  ```|```class Student extends Person ```|```class Student(Person): ```|
|default values |```def name(input='bezos') ```</br>```end```|```function(input='bezos')  ```|```def name(input='bezos') ```|


<h3 id=regex>Regular expression (Regex)</h3>
<p><em>where, lx = "titan titan titan"</em></p>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------| :-----|:--------|
|First occurrence |```lx.match(/t[a-z]*n/)[0]```|```(/t[a-z]*n/).test(lx) //=> true ```|```import re```</br>```re.search("t[a-z]*n", lx).group() ```|
|All occurrences |```lx.scan(/t[a-z]*n/)```|```lx.match(/t[a-z]*n/gi)```|```re.findall("t[a-z]*n",lx)```|

<h3 id=heredoc>Heredocs</h3>

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------| :-----|:--------|
| Multiline string |```content = <<~HEREDOC```</br>```I welcome your contributions.```</br>```please suggest```</br>```a topic ```</br>```or report an issue```</br>```HEREDOC```</br>```p content```|```  ```|```content = """ I welcome your contributions.```</br>```please suggest```</br>```a topic ```</br>```or report an issue```</br>```"""```</br>```print(content)```|
