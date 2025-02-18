
# Validation

```db.createCollection('Nonfiction'),{validator:{$jsonSchema:{required:['name', 'price']properties: {name: {$bsonTupe: 'string',description: 'must be a string '},price:{$bsonTupe: 'number',description: 'must be a number'}}},},validationAction: 'error'}```

# Modify validation

```db.runCommand('Nonfiction'),{validator:{$jsonSchema:{required:['name', 'price','author']properties: {name: {$bsonTupe: 'string',description: 'must be a string '},price:{$bsonTupe: 'number',description: 'must be a number'}}},},validationAction: 'error'}```

