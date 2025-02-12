to get only one column data

```db.students.find({}, {name:1})```
to get all names  right 1

```db.students.find({}, {name:1, _id:0})```

remove _id from search results becoz find by default gets _ids with search
