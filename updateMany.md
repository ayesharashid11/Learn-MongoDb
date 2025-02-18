
```db.students.updateOne({name:"Ayesha", age:12}, {$set:{age:20}})```


```db.students.updateMany({}, {$set:{hobbiies:['cooking']}})```

```db.students.updateMany({age:12}, {$set:{hobbiies:['cooking']}})```

```db.students.updateMany({}, {$in: {age:1}})```
increment age by one

```db.students.updateOne({name:'Sita'}, {$min: {age: 23}})```

```db.students.updateMany({}, {$mul: {age: 2}})```

$unset -> reset that field
$rename -> {$rename: {age: 'StudentAge'}}




