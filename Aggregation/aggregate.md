# Pipeline Operations
array of operations.
 it groups data from different docs in a single doc
 the output of one stage is the input of next stage.

 1. $match
 ```db.teachers.aggregate([{$match:{gender:"male"}}])```

 2. $group
 ```db.teachers.aggregate([{$group:{_id:"$age"}}])```
 id field int group stage specifies the field based on which docs will be gropued.
 this query returns groups with id

 ```db.teachers.aggregate([{$group:{_id:"$age", names: {$push: "$name}}}])```

 ```db.teachers.aggregate([{$group:{_id:"$age", students:{$push"$$ROOT}}}])```
 root value is the reference to current doc being processed in the pipeline, which reprsents the complete doc.

 ```db.teachers.aggregate([{$match:{gender:"male"}}, {$group:{_id:"$age", number:{$sum:1}}}])```

 ```db.teachers.aggregate([{$match:{gender:"male"}}, {$group:{_id:"$age", number:{$sum:1}}}, {$sort:{number:-1}}])```


 ```db.teachers.aggregate([{$group:{_id:"$age" hobbies:{$push:"$Hobbies"}}}])```

 3. $unwind

 ```db.teachers.aggregate([{$unwind: "$hobbies"}])```

 ```db.teachers.aggregate([{$unwind: "$hobbies"}, {$group:{_id:"$Hobbies",count:{$sum:1}}])```

 ```db.teachers.aggregate([{$group: {_id:null, avegAvg:{$avg:$age"}}}])```

 id=null , it will not group ids into seperate groups. rather it creates a single group












