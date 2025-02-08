```db.students.find()```

finds all documents

-> to find nested docs

```db.students.find({'idCards.hasBankCards': true})```

```db.students.find({age:{$lt:12}})```

find age less than 12

```db.students.find({age:{$lt:12, $gt:5}})```
