
```db.students.find({Hobbies: 'cricket'}).limit(5)```

```db.students.find({'experience.Company' : 'Amazon'})```

expience Array have Company obj

```db.students.find({Hobbies: 'cricket'}).size()```

```db.students.find({experience: {$size: 3}})```
calculates the size of an array and returns 3

```db.students.find({Hobbies: {$all:['Walking', 'Reading']}})```
if we do not write the $all it return exaclty the same pattern of array. the array may contain ['Reading', 'Walking'] , it will not return this doc. so write all. 



```db.students.find({course: {$selectMatch:{ quantity: {$gt:2}, {name:'computer'} }} })```

```db.students.find({experienc: {$elemMatch:{duration:{$lte:1}}}})```

this find duration in nested array of experince. duration is also an array.

```db.students.updateMany({experienc: {$elemMatch:{duration:{$lte:1}}}}, {$set:{"experience.$.neglect": true}})```

this returns the only first matched element in array and updates them. neglect:true will be added in doc.

```db.students.updateMany({experienc: {$elemMatch:{duration:{$lte:1}}}}, {$set:{"experience.$[].neglect": 1}})```

this returns the all matched element in array and updates them. neglect:1 will be added in doc.

```db.students.updateOne({name: "Ram"}, {$push: {experience: {comapny: "Meta"}, {duration: 2}}})```
adds doc in nested arrays



```db.students.updateOne({name: "Ram"}, {$addToSet: {experience: {comapny: "Meta"}, {duration: 2}}})```
it checks if doc already exists it do not adds it.

```db.students.updateOne({name: "Ram"}, {$pull: {experience: {comapny: "Meta"}, {duration: 2}}})```
removes the doc from array

```db.students.updateOne({name: "Ram"}, {$pop: {experience: 1}})```
removes doc from nested last.

```db.students.updateOne({name: "Ram"}, {$pop: {experience: -1}})```
removes doc from start of nested array
