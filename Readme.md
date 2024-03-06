Certainly! Below is the README content for your MongoDB cheatsheet repository:

---

# MongoDB Cheatsheet

A handy cheatsheet for MongoDB users to reference basic and advanced commands without the need to search for each command online.

## MongoDB Shell Cheatsheet

### Basic Commands

1. **Start MongoDB Shell:**
   ```
   mongo
   ```

2. **View Databases:**
   ```
   show dbs
   ```

3. **Switch Database:**
   ```
   use mydatabase
   ```

4. **View Collections in Current Database:**
   ```
   show collections
   ```

5. **Create Database:**
   ```
   use mydatabase
   ```

6. **Create Collection:**
   ```
   db.createCollection("mycollection")
   ```

7. **Insert Document into Collection:**
   ```
   db.mycollection.insertOne({ key: "value" })
   ```

8. **Find Documents in Collection:**
   ```
   db.mycollection.find()
   ```

9. **Update Document in Collection:**
   ```
   db.mycollection.updateOne({ key: "value" }, { $set: { key: "new value" } })
   ```

10. **Remove Document from Collection:**
    ```
    db.mycollection.deleteOne({ key: "value" })
    ```

11. **Drop Collection:**
    ```
    db.mycollection.drop()
    ```

12. **Drop Database:**
    ```
    use mydatabase
    db.dropDatabase()
    ```

### Advanced Commands

13. **Index Management:**
    - Create Index: `db.mycollection.createIndex({ key: 1 })`
    - List Indexes: `db.mycollection.getIndexes()`
    - Drop Index: `db.mycollection.dropIndex("indexName")`

14. **Aggregation Framework:**
    ```
    db.mycollection.aggregate([...])
    ```

15. **Data Import and Export:**
    - Import Data from JSON: `mongoimport --db mydatabase --collection mycollection --file data.json`
    - Export Data to JSON: `mongoexport --db mydatabase --collection mycollection --out data.json`

16. **User Management:**
    - Create User: `db.createUser({ user: "username", pwd: "password", roles: ["readWrite"] })`
    - List Users: `db.getUsers()`
    - Drop User: `db.dropUser("username")`

17. **Replica Sets and Sharding:**
    - Initialize Replica Set: `rs.initiate()`
    - Add Replica Set Member: `rs.add("hostname:port")`
    - Enable Sharding on Database: `sh.enableSharding("mydatabase")`
    - Shard Collection: `sh.shardCollection("mydatabase.mycollection", { shardKey: 1 })`

18. **Server Administration:**
    - Server Status: `db.serverStatus()`
    - Current Operations: `db.currentOp()`
    - Server Logs: `db.getLog("global")`

Feel free to copy and paste these commands into your MongoDB terminal for quick reference!

---

You can copy the content and save it into your README.md file in your MongoDB cheatsheet repository. This will provide users with an easy-to-access reference for MongoDB commands.
