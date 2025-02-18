
```db.students.find({Hobbies: 'cricket'}).limit(5)```

```db.students.find({'experience.Company' : 'Amazon'})```

expience Array have Company obj

```db.students.find({Hobbies: 'cricket'}).size()```

```db.students.find({experience: {$size: 3}})```
calculates the size of an array and returns 3

```db.students.find({Hobbies: {$all:['Walking', 'Reading']}})```
if we do not write the $all it return exaclty the same pattern of array. the array may contain ['Reading', 'Walking'] , it will not return this doc. so write all. 



```db.students.find({course: {$selectMatch:{ quantity: {$gt:2}, {name:'computer'} }} })```