# MongoDB Data Insertion Documentation

This documentation will guide you through the process of inserting the provided JSON data into the "songsDB" MongoDB database with three collections: "artists," "songs," and "popularsongs."

## Prerequisites

Before proceeding, ensure that you have the following:

1. MongoDB installed on your system.
2. MongoDB Server running.
3. MongoDB Shell (mongo) accessible from your command line.

## Inserting Data into the "artists" Collection

To insert data into the "artists" collection, follow these steps:

1. **Access the MongoDB Shell:**

   Open your terminal or command prompt and access the MongoDB Shell by typing `mongo` and pressing Enter.

2. **Choose the "songsDB" Database:**

   Use the `use` command to switch to the "songsDB" database. If the database doesn't exist, MongoDB will create it when you first insert data.

   ```javascript
   use songsDB
   ```

3. **Insert Data into the "artists" Collection:**

   Insert the provided JSON data into the "artists" collection using the `insertMany` method. Run the following command:

   ```javascript
   db.artists.insertMany([
     {
       "_id": {
         "$oid": "64b6bef8f716102491b47d2b"
       },
       "name": "Taylor Swift",
       "birthDate": {
         "$date": "1989-12-12T17:00:00.000Z"
       },
       "genres": ["pop", "country", "folk", "rock"]
     },
     // Insert other artist objects here...
   ]);
   ```

   Replace the comments (`// Insert other artist objects here...`) with the remaining artist objects from the provided JSON data.

4. **Verify the Insertion:**

   To verify that the data has been inserted successfully, you can use the `find` method to retrieve the inserted data from the "artists" collection. For example, to retrieve all documents from the "artists" collection, use the following command:

   ```javascript
   db.artists.find({});
   ```

   This will display all documents from the "artists" collection, including the ones you inserted.

## Inserting Data into the "popularsongs" Collection

To insert data into the "popularsongs" collection, follow these steps:

1. **Access the MongoDB Shell:**

   If you're already in the MongoDB Shell, proceed to the next step. Otherwise, open your terminal or command prompt and access the MongoDB Shell by typing `mongo` and pressing Enter.

2. **Choose the "songsDB" Database:**

   If you're already in the "songsDB" database, proceed to the next step. Otherwise, use the `use` command to switch to the "songsDB" database.

   ```javascript
   use songsDB
   ```

3. **Insert Data into the "popularsongs" Collection:**

   Insert the provided JSON data into the "popularsongs" collection using the `insertMany` method. Run the following command:

   ```javascript
   db.popularsongs.insertMany([
     {
       "_id": { "$oid": "64b6cd333d7c4eefcf23cd78" },
       "title": "Cruel Summer",
       "timePlayed": 532
     },
     // Insert other popular song objects here...
   ]);
   ```

   Replace the comments (`// Insert other popular song objects here...`) with the remaining popular song objects from the provided JSON data.

4. **Verify the Insertion:**

   To verify that the data has been inserted successfully, you can use the `find` method to retrieve the inserted data from the "popularsongs" collection. For example, to retrieve all documents from the "popularsongs" collection, use the following command:

   ```javascript
   db.popularsongs.find({});
   ```

   This will display all documents from the "popularsongs" collection, including the ones you inserted.

