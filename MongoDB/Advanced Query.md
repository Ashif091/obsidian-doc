-  [[StartTransaction]]

```js
db.products.find().forEach(function(doc) {
    db.products.updateOne(
        { _id: doc._id },
        { $set: { price: parseFloat(doc.price) } }
    );
});
```

field exists or not 
```js
db.products.deleteMany({ exp_date: { $exists: false } });
```

```js
 db.products.updateMany({},[{$set:{price:{$toInt:'$price'}}}])
```

```js
db.products.find({
  $expr: {
    $not: {
      $regexMatch: {
        input: "$name",
        regex: /Monit/i
      }
    }
  }
})

```

#### change the first prefix to upper or lower ?
```js
db.products.updateMany(
  {},
  [
    {
      $set: {
        name: {
          $concat: [
            { $toUpper: { $substrCP: ["$name", 0, 1] } },
            { $substrCP: ["$name", 1, { $strLenCP: "$name" }] }
          ]
        }
      }
    }
  ]
);

```

#### Setting the date in a doc 

```js
db.events.insertOne({ title: 'Sample Event', eventDate: new Date() });
```

```js
db.events.updateOne(
  { _id: ObjectId('your_document_id') },
  {
    $set: {
      title: 'Sample Event',
      eventDate: { $currentDate: { $type: 'date' } }
    }
  }
);
```

#### pagination 
```js
const page = 2; // The current page number
const postsPerPage = 10;

// Calculate the number of documents to skip
const skipCount = (page - 1) * postsPerPage;

// Query the database to get the posts for the current page
db.posts.find().skip(skipCount).limit(postsPerPage);
```

#### bulkWrite 
```js 
const operations = [
  {
    updateOne: {
      filter: { _id: 1 },
      update: { $set: { price: 29.99 } }
    }
  },
  {
    updateOne: {
      filter: { _id: 2 },
      update: { $set: { price: 19.99 } }
    }
  },
  {
    insertOne: {
      document: { _id: 3, name: "New Product", price: 39.99 }
    }
  },
  // You can include more operations here
];

// Execute the bulk write
db.collection.bulkWrite(operations);
```
#### max & min type Q 

```js
db.products.aggregate([
  {
    $sort: { price: 1 } // Sort by price in ascending order
  },
  {
    $limit: 1 // Limit the results to the first document
  },
  {
    $project: { name: 1, _id: 0 } // Project only the name field
  }
])

```