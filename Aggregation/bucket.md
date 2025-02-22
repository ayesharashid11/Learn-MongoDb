used when we need to categorize into discrete groups based on specified boundries.

Suntax:
{
    $bucket:{
        groupBy: <expression>,
        bounderies:[
            <boundary1>,,,,    
        ],
        default: <expression>,
        output:{
            <outputField>:{<accumulator>:<expression>}
        }
    }
}

 ```db.teachers.aggregate([{$match:{gender:"male"}}, {4bucket: {groupBy:"$age", boundaries:[0, 30, 40], default: 'Greater than 40', output:{count:{$sum: 1}}}}])```

