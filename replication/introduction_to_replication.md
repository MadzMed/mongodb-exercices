# Exercise: Setting Up MongoDB Replication on Localhost

## Objective:

You will learn how to set up a MongoDB replication set with one primary and two secondary nodes on localhost. They will also create a database named with their last name, insert data into a collection in the primary node, and verify the asynchronous replication to the secondary nodes.

## Instructions

In this exercise, you will set up a replica set on your local machine. You will use the `mongod` command to start three `mongod` instances, each running on a different port. You will then connect to one of the instances and initiate a replica set.

### Step 1: Start the `mongod` instances

1. start creating a directory `data` and three subdirectories `db1`, `db2`, and `db3` in the terminal.

2. Open the mongodb configuration file `mongod.conf` in a text editor and enable the replication by adding the following lines:

   ```plaintext
   replication:
      replSetName: 'rs0'
   ```

3. Start a first `mongod` instance on port 27017, using the `db1` directory for the data files and the `mongod.conf` file for the configuration. Take a look to the flags `--replSet` and `--port`

4. Start a second `mongod` instance on port 27018, using the `db2` directory for the data files and the `mongod.conf` file for the configuration.

5. Start a third `mongod` instance on port 27019, using the `db3` directory for the data files and the `mongod.conf` file for the configuration.

### Step 2: Connect to one of the `mongod` instances

1. Connect to the first `mongod` instance on port 27017 using the `mongo` or `mongosh` shell.

2. Initialize the replica set.

3. Add the second and third `mongod` instances to the replica set.

4. Verify that the replica set is working correctly. hint: `rs.status()`

### Step 3: Create a database and insert data

1. Create a database named GameOfThrones.

2. Create a collection named characters.

3. Insert the following documents into the collection:

   ```plaintext
   { name: 'Jon Snow', age: 25, house: 'Stark' }
   { name: 'Daenerys Targaryen', age: 23, house: 'Targaryen' }
   { name: 'Tyrion Lannister', age: 30, house: 'Lannister' }
   ```

### Step 4: Verify the replication

1. Connect to the second `mongod` instance on port 27018 using the `mongo` or `mongosh` shell.

2. Query the `GameOfThrones` database and the `characters` collection to verify that the data has been replicated.

3. Can you read the data ? Can you write the data ?

4. Connect to the third `mongod` instance on port 27019 using the `mongo` or `mongosh` shell.

5. Query the `GameOfThrones` database and the `characters` collection to verify that the data has been replicated.

6. Can you read the data ? Can you write the data ?

### Step 5: Shutdown the first `mongod` instance

1. Shutdown the first `mongod` instance on port 27017.

2. Verify that the second `mongod` instance has been elected as the new primary.

3. Verify that the third `mongod` instance is still a secondary.

### Step 6: Cleanup

1. Shutdown the second and third `mongod` instances.

2. Delete the `db1`, `db2`, and `db3` directories.