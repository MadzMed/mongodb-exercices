# Writing Scripts for Creating and Restoring Backups on MongoDB Atlas

## Objective:

Students will learn how to write scripts for creating and restoring backups on MongoDB Atlas using the `mongodump` and `mongorestore` commands.

## Prerequisites:

- MongoDB Atlas account with an active cluster
- Basic knowledge of bash scripting and the MongoDB Atlas API
- curl installed on your local machine

## Steps:

1. Setup MongoDB Atlas API Access:
    
    - Go to the MongoDB Atlas dashboard and navigate to the "Access Manager" section.
    - Create a new API key with the necessary permissions to access your cluster.
    - Note down the public and private keys generated for the API key.

2. Script for Creating Backups:

    - Write a bash script that uses curl to interact with the MongoDB Atlas API and create a backup snapshot.
    - Use the `mongodump` command to create a backup of your MongoDB cluster data.

3. Script for Restoring Backups:

    - Write a bash script that uses curl to interact with the MongoDB Atlas API and restore a backup snapshot.
    - Use the `mongorestore` command to restore the backup data to your MongoDB cluster.

4. Make the Scripts Executable:

    - Set the executable permission for the backup and restore scripts using the `chmod` command.
    - Ensure that the scripts are saved in a secure location and accessible only to authorized users.

5. Test the Backup and Restore Scripts:

    - Run the backup script to create a backup of your MongoDB cluster data.
    - Verify that the backup snapshot is created successfully.
    - Run the restore script to restore the backup data to your MongoDB cluster.
    - Verify that the data is restored correctly and the cluster is operational.

## Expected Outcomes:

- Students should understand how to use bash scripts to interact with the MongoDB Atlas API for creating and restoring backups.
- The report should detail the steps taken, any challenges faced, and the final outcome of the backup and restore operations.

## Summary:

By writing scripts for creating and restoring backups on MongoDB Atlas, you can automate the backup process and ensure data integrity and availability. These scripts provide a convenient way to manage backups and streamline the recovery process in case of data loss or system failures.