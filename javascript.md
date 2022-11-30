In Mongo we can use declaration from javascript like this:

```mongodb
mongo> x = 200
200
mongo> x
200
mongo> x/5
40
mongo> x*4
800
mongo> x * 3
600
mongo> Math.sin(Math.PI/2)
1
mongo> new Date()
ISODate("2022-11-29T18:20:27.103Z")
mongo> new Date("2019/1/1")
ISODate("2019-01-01T06:00:00.000Z")
```
We can declarate functions in mongo like this:

```mongodb
mongo> function factorial(n){if (n<=1) return 1; return n*factorial(n-1)}
[Function: factorial]
mongo> factorial(5)
120
```

