# MongoDB_02
**1. Create a Database called customers.**

    Movies> use customers switched to db customers customers>
    
**2. Create a collection called customerdetails.**

    customers> db.createCollection(“customersdetails”) { ok: 1 } customers>

**3. Insert all documents into the collection named   customerdetails.**

    customers> db.customerdetails.insertMany([{“name”:”John”,”age”:”25”,”gender”:”Male”,”city”:”New York”},{“name”:”Emily”,”age”:”25”,”gender”:”Female”,”city”:”London”},            {“name”:”Daniel”,”age”:”22”,”gender”:”Male”,”city”:”Sydney”},{“name”:”Sophia”,”age”:”28”,”gender”:”Female”,”city”:”Paris”},{“name”:”William”,”age”:”26”,”gender”:”Male”,”city”:”Chicago”},{“name”:”Olivia”,”age”:”23”,”gender”:”Female”,”city”:”Los Angeles”},{“name”:”Benjamin”,”age”:”27”,”gender”:”Male”,”city”:”Toronto”},{“name”:”Mila”,”age”:”30”,”gender”:”Female”,”city”:”Berlin”},{“name”:”James”,”age”:”30”,”gender”:”Male”,”city”:”Tokyo”}]) 

**4. Retrieve all documents from the collection and sort the results by the “age” field    in ascending order.**

    customers> db.customerdetails.find().sort({age:1}).pretty() [ { _id: ObjectId(“654cb0a8a1791bba19b7e11f”), name: ‘Daniel’, age: ‘22’, gender: ‘Male’, city: ‘Sydney’ }, { _id:     ObjectId(“654cb0a8a1791bba19b7e122”), name: ‘Olivia’, age: ‘23’, gender: ‘Female’, city: ‘Los Angeles’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e11d”), name: ‘John’, age: ‘25’, gender: ‘Male’, city: ‘New York’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e11e”), name: ‘Emily’, age: ‘25’, gender: ‘Female’, city: ‘London’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e121”), name: ‘William’, age: ‘26’, gender: ‘Male’, city: ‘Chicago’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e123”), name: ‘Benjamin’, age: ‘27’, gender: ‘Male’, city: ‘Toronto’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e120”), name: ‘Sophia’, age: ‘28’, gender: ‘Female’, city: ‘Paris’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e124”), name: ‘Mila’, age: ‘30’, gender: ‘Female’, city: ‘Berlin’ }, { _id: ObjectId(“654cb0a8a1791bba19b7e125”), name: ‘James’, age: ‘30’, gender: ‘Male’, city: ‘Tokyo’ } ]

**5.Count the number of females. **

customers> db.customerdetails.countDocuments({“gender”:”Female”}) 4




**6.Insert one document into the customerdetails collection.**

**7. Update city=SriLanka to John.**

**8. Remove the customer from Tokyo.**

**9. Find customers not from Los Angeles.**
**10.Find the customers who are older than age 25.**
**11.Retrieve the males who are less than 25.**
**12.Update Francis age to 35, if Francis is not available upsert.**
**13.Retrieve males who are younger than 30 and older than25.**
**14.Find a customer who is lesser than or equal to 23.**

