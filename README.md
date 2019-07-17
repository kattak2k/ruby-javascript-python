# Cheat sheet: Ruby vs Javascript vs Python
An analogy between the Ruby, Javascript and Python languages


| Description   |Ruby           | Javascript     |Python |
| ------------- |:--------------:| :-----:|:--------:|
| Start Cli| irb | python | node |
| Integers & floats declaration    |``` x = 1 ; y = 0.23 ```|``` let x = 1; var y = 0.23 ```|```x = 1 ; y = 0.23```|
| Contants Declaration     |``` W = 'ruby'.freeze ```|``` const w = 'js' ```|``` W = 'ruby' ```|
| Variables in strings     |``` "one is #{x}" ```|``` `one is ${w}\` ```|``` "one is {}".format(x) ```|
| Line Comment            |``` # this is comment ```|``` // this is comment ```|``` # this is comment ```| 
| Block comments |```=being ;  =end ```|``` /* block comment */ ```|``` ''' block comment ''' ```|
| write output |``` puts 'write output' ```|```console.log('write output') ```|```print('write output')```|
| Arrays , Lists    |``` arr = [1,'a',true] ; arr = Array.new ```|```let arr = [1,'a',true]```|``` arr = [1,'a',True] ```|
| Hashes, Objects, dictionaries |```hash = { 'a' => 2, :b => 4 }```|```var obj = { 1 : 2 , 'a' : 4}```|```dict = {1: 2, 'd': 'e' }```|
| Destructuring |``` a,b,c = [2,3,4] ; p b```|``` var {x : a , y: b} = {x : 1, y : 2} ; console.log(b) ```|```a,b,c = [2,3,4]```|



## Arrays Functions where x is [3,4,5,6,7,8]

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
|index|```x.index(3)```|```x.indexOf(3)```|```x.index(3)```|
|insert|```x.insert(2, 'Feb')```|```x.splice(1, 0, 'Feb')```|```x.insert(2, 'Feb')```|
| Make a copy|```y = x.dup ```|```let y = [...x] ```|``` y = x[:] ```|
| Select, filter |```x.select{\|el\| el > 4 }```|```x.filter((el)=> el > 4)```|```filter(lambda el: el > 4, x)```|
| Reduce |```x.reduce(:+)```|```lx.reduce((result,el)=> result + el,0) ```|```reduce(lambda result,y: result + y, x) ```|
| Map |```x.map{\|el\| el*2}```|```lx.map((el)=> el*2) ```|```map(lambda el: el*2,x)```|
| Each |``` z = []```  </br> ``` x.each{\|el\| z << el*2}``` </br> ```p z ``` |```let z = []``` </br> ```lx.forEach((el) => z.push(el * 2))``` </br> ```console.log(z)```|``` for e in y: ``` </br> ```z.append(e * 2)```</br> ```print z ```|
| Reverse loop |``` z = []```  </br> ``` x.reverse_each{\|el\| z << el*2}``` </br> ```p z ``` |```let z = []``` </br> ```x.slice().reverse().forEach((el) => z.push(el * 2))``` </br> ```console.log(z)```|``` for e in range(len(x) - 1, -1,-1): ``` </br> ```z.append(e * 2)```</br> ```print z ```|
| Clear , Reset |```x.clear```|```x = [] ```|```del x[:]```|

  
## Working with multiple arrays. where, x is [1,2,3] & y is [2,4,5,6]

| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------:| :-----:|:--------:|
|Intersection|```x & y #=> [2]```|```x.filter(e => y.includes(e)) ```|```list(set(x) & set(y)) ```|
|Union|```x \| y```</br>```x.union(y)```|```var z = [...x,...y]```</br>```[...new Set( z )]```</br> 'or'```Array.from(new Set(z)) ```|```list(set(x) \| set(y)) ```|
|Join|```x + y```|```[...x,...y] ```|```x + y```|
|Difference|```x - y```|```x.filter(e => !y.includes(e)); ```|``` list(set(x) - set(y))```|

## Logical Conditions
| Description   |Ruby           | Javascript     |Python |
| :------------- |:--------------| :-----|:--------|
| If |```if <condition1>```</br>```elsif <condition2> ```</br>```else ```</br> ```end```|```if <condition1>:```</br>``` elif <condition2>:```</br> ``` else:```|```if (<condition1>) {```</br>```} else if (<condition2>) {```</br>```} else {```</br>```} ```|  


