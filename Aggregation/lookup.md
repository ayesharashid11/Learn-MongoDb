the $lookup is an aggregation pipeline stage that allows you to perform a left outer join b/w two collections

Syntax:
db.collection.aggregation([
    {
        $lookup:{
            from: "foriegnCollection",
            localField: "localField",
            foreignField: "foreignField",
            as: "outputArray(fieldName)
        }
    }
])