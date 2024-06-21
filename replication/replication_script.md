# Exercise: Write a script to set up MongoDB replication on localhost

## Objective:
Create a bash script that sets up MongoDB replication on localhost by creating a replica set.

## Instructions 

1. Create a new bash script file named `replication_script.sh`.

2. Add a shebang line to specify the shell to use.

3. Define three variables `PORT1`, `PORT2`, and `PORT3` with the values `27017`, `27018`, and `27019` respectively.

4. Create three directories `db1`, `db2`, and `db3` to store the data files for each `mongod` instance.

5. Start the first `mongod` instance on `PORT1` using the `db1` directory for the data files and the `mongod.conf` file for the configuration.

6. Start the second `mongod` instance on `PORT2` using the `db2` directory for the data files and the `mongod.conf` file for the configuration.

7. Start the third `mongod` instance on `PORT3` using the `db3` directory for the data files and the `mongod.conf` file for the configuration.

8. Connect to one of the `mongod` instances and initialize the replica set with the name `rs0`.

9. Add the second and third `mongod` instances to the replica set.

10. Run the script.

11. Verify that the replica set is working correctly by checking the status of the replica set.