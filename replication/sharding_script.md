# Exercice: Write a script to set up MongoDB sharding on localhost

## Objectif:
Create a bash script that sets up MongoDB sharding on localhost by creating a sharded cluster.

## Setup:

1. Create three config files named `mongod_shard.conf`, `mongod_config.conf`, and `mongos.conf` to store the configuration for the `mongod` instances, config server, and mongos respectively.

2. Create a new directory named `data` and three subdirectories `configdb`, `shard1`, and `shard2` to store the data files for the config server and shard servers.

## Instructions

1. Create a new bash script file named `sharding_script.sh`.

2. Add a shebang line to specify the shell to use.

3. Define three variables `PORT1`, `PORT2`, and `PORT3` with the values `27018`, `27019`, and `27020` respectively.

4. Create three directories `shard1`, `shard2`, and `shard3` to store the data files for each `mongod` instance.

5. Start the first `mongod` instance on `PORT1` using the `shard1` directory for the data files and the `mongod_shard.conf` file for the configuration.

6. Start the second `mongod` instance on `PORT2` using the `shard2` directory for the data files and the `mongod_shard.conf` file for the configuration.

7. Start the third `mongod` instance on `PORT3` using the `shard3` directory for the data files and the `mongod_shard.conf` file for the configuration.

8. Start the config server on port 27017, using the `configdb` directory for the data files and the `mongod_config.conf` file for the configuration.

9. Connect to the config server using the MongoDB shell.

10. Initialize the config server.

11. Enable sharding for a specific database.

12. Shard a collection within the database.

13. Run the script.

14. Verify that the sharding setup is working correctly by running the following command in the MongoDB shell:
```
sh.status()
```

15. Get the number of chunks in the `realEstate` collection using the following command:
```
db.realEstate.getShardDistribution()
```

16. Verify that the data is distributed across the shards by running the following command:
```
db.realEstate.find().explain("executionStats")
```

17. Verify that the data is being distributed across the shards by inserting new documents into the `realEstate` collection and checking the distribution.

18. Clean up the sharded cluster by removing the shards and config server.

19. Stop the `mongod` instances and config server.
