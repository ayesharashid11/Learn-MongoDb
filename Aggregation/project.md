It allows you to customize te output of your aggregation query by secifying which fields to inculde or exclude.


```db.emp.collection([$project:{firstName: 1, lastname:1,_id:0}])```