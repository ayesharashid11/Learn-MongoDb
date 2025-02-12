
```db.students.insertOne({name: "Ram" , Age: 12})```


```db.students.insertMany([{name: "Ayesha" , Age: 12},{name: "Rashid" , Age: 12}])```

# OPTIONS

```db.students.insertMany([{name: "Ayesha" , Age: 12},{name: "Rashid" , Age: 12}], {ordered:false})```

if we have any error in between inserting doc. it forcefulu adds all docs
