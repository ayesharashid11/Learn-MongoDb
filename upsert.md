

```db.students.updateOne({name:'Sita'}, {$set:{hobbiies:['cooking']}}, {upsert:true})```


upsert inserts a new doc if not created already
