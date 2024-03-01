# Python-and-MongoDB

## Exploring the Relationship between Python and MongoDB

This repository contains materials for a presentation that delves into the relationship between Python and MongoDB. 

### Presentation Outline:

1. **Introduction to Python:**
   - Overview of Python programming language
   - Key features and strengths of Python
   - Python's popularity and use cases

2. **Introduction to MongoDB:**
   - Overview of MongoDB database
   - Key features and strengths of MongoDB
   - MongoDB's popularity and use cases

3. **Why Python and MongoDB?**
   - Compatibility between Python and MongoDB
   - Advantages of using Python with MongoDB
   - Real-world examples showcasing the synergy between the two technologies

4. **Python Drivers for MongoDB:**
   - Overview of popular Python drivers for MongoDB (e.g., PyMongo)
   - Installation and setup instructions
   - Basic usage examples
   
   ```python
   # Basic usage example of PyMongo
   
   from pymongo import MongoClient
   
   # Connect to MongoDB
   client = MongoClient('mongodb://localhost:27017/')
   
   # Select database
   db = client['mydatabase']
   
   # Select collection
   collection = db['mycollection']
   
   # Insert document
   collection.insert_one({'key': 'value'})
   
   # Find document
   result = collection.find_one({'key': 'value'})
   
   # Print result
   print(result)



   # 5. CRUD Operations with Python and MongoDB:

   # Create - Inserting multiple documents
   collection.insert_many([
    {'name': 'John', 'age': 30},
    {'name': 'Alice', 'age': 25},
    {'name': 'Bob', 'age': 35}
   ])

     # Read - Find documents
    results = collection.find({'age': {'$gte': 30}})
   for result in results:
    print(result)

   # Update - Update a document
   collection.update_one({'name': 'John'}, {'$set': {'age': 32}})

# Delete - Delete a document
collection.delete_one({'name': 'Alice'})

