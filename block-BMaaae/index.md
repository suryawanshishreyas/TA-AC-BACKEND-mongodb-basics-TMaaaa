writeCode

Write code here:-

- create a database named `sports`.
  > > use sports
- list all databases present in local mongod server.
  > > show dbs
- create 3 collections named `cricket`, `football`, `TT` in sports databse.
  > > db.createCollection('cricket')
  > > db.createCollection('football')
  > > db.createCollection('TT')
- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
  > > db.cricket.insertMany([{name:'Rohit'}, {age:38}, {email:'hitman@gmail.com'}, {bid_price:'30CR'}])
  > > db.football.insertMany([{name:'Lionel'}, {age:37}, {email:'goat@gmail.com'}, {bid_price:'3000CR'}])
  > > db.TT.insertMany([{name:'Rohan'}, {age:25}, {email:'rohanchamp@gmail.com'}, {bid_price:'12LPA'}])
- list all collections in sports database.
  > > show collections
- rename `TT` collection to `tennis`.
  > > db.TT.renameCollection('tennis')
- create a capped collection called `khokho` which should have max 3 documents.

  > > db.createCollection('khokho', {capped:true, size:100000, max:3})
  > > db.khokho.insertMany([{name:'xxx'}, {age:'xxx'},{ email:'xxx'},{price:'xxx'}])

  -Try inserting more than 3 and see what happens?

  > > db.khokho.insertOne({heihgt:'170CM'})

- check whether a collection is capped or not?
  > > db.khokho.isCapped()
- drop all documents from `football` collection.
  > > db.football.drop()
- delete cricket collection completely.
  > > db.cricket.drop()
- delete sports database.
  > > db.dropDatabase()
- check which database you are connected to ?
  > > db
- connect to test database
  > > use test
