
``` db.student.find({age: 5})```

``` db.student.find({age: {$eq: 5}})```

``` db.student.find({age: {$ne: 5}})```

``` db.student.find({age: {$in: [2, 5, 7]}})```


``` db.student.find($or:[ {age: {$lte: 10}, {age: {$gte: 20}}])```

``` db.student.find($nor:[ {age: {$lte: 10}, {age: {$gte: 20}}])```

``` db.student.find($and:[ {age: {$lte: 10}, {age: {$gte: 20}}])```


