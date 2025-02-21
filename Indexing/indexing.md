# Indexing

It stores:
- index keys
- Pointers to the documents in the collection.
- helps in sorting
The index is stored in memory.
The index is updated when a document is inserted, updated or deleted.

When a query is executed MongoDb can use the index to quickly locate the doc that match the query by searching through Balance-tree.

# Trade Off
it consumes storage space 
it affects write/ update performance.


```db.teachers.createIndex({age:1})```

```db.teachers.getIndexes({age:1})```

```db.teachers.dropIndex("age:1")```  OR

```db.teachers.dropIndex({age:1})```
1 -> ascending order 
-1 -> descending order

Donot use collection when it is small. When the collection is frequently updated.
when the queries are complex. when the collection is large

```db.teachers.dropIndex({age:1}, {unique: true})```

```db.teachers.createIndex({age:1, gender:1})```
compound indexing


# Partial Filters

```db.teachers.createIndex({age:1}, partialFilterExpression:{age: {$gt: 22}})```

# Array Indexing

mongoDb create separate index entry for each value in each array.

# Text Index
one collection can have only single index