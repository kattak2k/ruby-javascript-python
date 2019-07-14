# Cheat sheet: Ruby vs Javascript vs Python
Similarities between Ruby, Javascript and Python languages


| Description   |Ruby           | Javascript     |Python |
| ------------- |:--------------:| :-----:|:--------:|
| Integers & floats declaration    |``` x = 1 ; y = 0.23 ```|``` let x = 1; var y = 0.23 ```|```x = 1 ; y = 0.23```|
| Contants Declaration     |``` W = 'ruby'.freeze ```|``` const w = 'js' ```|``` W = 'ruby' ```|
| Variables in strings     |``` "one is #{x}" ```|``` `one is ${w}\` ```|``` "one is {}".format(x) ```|
| Line Comment            |``` # this is comment ```|``` // this is comment ```|``` # this is comment ```| 
| Block comments |```=being ;  =end ```|``` /* block comment */ ```|``` ''' block comment ''' ```|
| write output |``` puts 'write output' ```|```console.log('write output') ```|```print('write output')```|
| Arrays declaration     |``` arr = [1,'a',true] ; arr = Array.new ```|```let arr = [1,'a',true]```|``` arr = [1,'a',True] ```|
| Hashes, Objects, dictionaries |```hash = { 'a' => 2, :b => 4 }```|```var obj = { 1 : 2 , 'a' : 4}```|```dict = {1: 2, 'd': 'e' }```|
| Destructuring |``` a,b,c = [2,3,4] ; p b```|``` var {x : a , y: b} = {x : 1, y : 2} ; console.log(b) ```|```a,b,c = [2,3,4]```|
| Array select, filter |```x.select{\|el\| el > 4 }```|```x.filter((el)=> el > 4)```|```filter(lambda el: el > 4, x)```|
| Array reduce |```x.reduce(:+)```|```lx.reduce((result,el)=> result + el,0) ```|```reduce(lambda result,y: result + y, x) ```|
| Array map |```x.map{\|el\| el*2}```|```lx.map((el)=> el*2) ```|```map(lambda el: el*2,x)```|


