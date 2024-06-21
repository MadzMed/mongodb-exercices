# Exercise: Setting Up MongoDB Sharding on Localhost

## Objective:
The objective of this exercise is to set up MongoDB sharding on localhost.
In this exercise, you will set up a sharded cluster on your local machine. You will use the `mongod` command to start multiple `mongod` instances, each running on a different port. You will then connect to the config server and shard servers to initialize the sharding setup.

## Setup:

1. Create a new database named `sharding_db`.

2. Create a new collection named `realEstate` in the `sharding_db` database.

3. Import the csv file from the `data` directory into the MongoDB database.

## Instructions:

1. create a directory `data` and three subdirectories `configdb`, `shard1`, and `shard2` in the terminal.

2. Start two `mongod` instances on ports 27018 and 27019, using the `shard1` and `shard2` directories for the data files respectively. Use the `mongod_shard.conf` file for the configuration. Take a look at the `--shardsvr` flag.

3. Start the config server on port 27017, using the `configdb` directory for the data files. Take a look at the `--configsvr` flag.

4. Connect to the config server using the MongoDB shell.

5. Initialize the config server. Take a look at the `sh.addShard()` command.

6. Enable sharding for a specific database. Take a look at the `sh.enableSharding()` command.

7. Shard a collection within the database. Take a look at the `sh.shardCollection()` command.

8. Verify that the sharding setup is working correctly by running the following command in the MongoDB shell:
```
sh.status()
```

9. Get the number of chunks in the `realEstate` collection using the following command:
```
db.realEstate.getShardDistribution()
```

10. Verify that the data is distributed across the shards by running the following command:
```
db.realEstate.find().explain("executionStats")
```

11. Verify that the data is being distributed across the shards by inserting new documents into the `realEstate` collection and checking the distribution.

12. Clean up the sharded cluster by removing the shards and config server. Take a look at the `sh.removeShard()` and `sh.removeShardTag()` commands.

13. Stop the `mongod` instances and config server.
