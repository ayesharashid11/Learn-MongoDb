bydefault mongodb prints only 20 dcosuments. use printjson medthod to print docs in one go 


```db.students.find().forEach(x => printEach(x))```
