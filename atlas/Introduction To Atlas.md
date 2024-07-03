# Deploying MongoDB Cluster on Atlas

## Objective:

Students will learn how to deploy a MongoDB cluster on MongoDB Atlas, configure access, and verify the setup by connecting to the cluster.

## Prerequisites:

- MongoDB Atlas account (can be created for free)

- Basic understanding of MongoDB and its command-line interface

## Instructions:

1. **Create a MongoDB Atlas Account:**
    
    - Go to the [MongoDB Atlas website](https://www.mongodb.com/cloud/atlas) and sign up for a free account.

    - Once you have signed up, log in to your account.

2. **Configure the Organization and Project:**
        
    - After logging in, you will be prompted to create an organization and a project.

    - An organization is a group of projects, and a project is a group of clusters.

    - You can create a new organization or use an existing one.

    - Create a new project or use an existing one.

3. **Create a New Cluster:**

    - Click on the "Build a Cluster" button to create a new cluster.
    
    - Choose the cloud provider and region where you want to deploy the cluster.
    
    - Select the cluster tier (e.g., M0, M2, M5, etc.).
    
    - Configure additional settings like the cluster name, backup options, etc.
    
    - Click on the "Create Cluster" button to deploy the cluster.

4. **Configure Access:**

    - Click on the "Database Access" tab in the left sidebar.
    
    - Click on the "Add New Database User" button to create a new user.
    
    - Enter the username and password for the new user.
    
    - Configure the user's privileges (e.g., read/write access to specific databases).
    
    - Click on the "Add User" button to save the user.

5. **Whitelist IP Addresses:**

    - Click on the "Network Access" tab in the left sidebar.
    
    - Click on the "Add IP Address" button to whitelist an IP address.
    
    - Enter the IP address or CIDR block you want to whitelist.
    
    - Click on the "Confirm" button to save the IP address.

6. **Connect to the Cluster:**

    - Click on the "Clusters" tab in the left sidebar.
    
    - Click on the "Connect" button for the cluster you want to connect to.
    
    - Choose the connection method (e.g., MongoDB Shell, MongoDB Compass, etc.).
    
    - Follow the instructions to connect to the cluster using the selected method.

7. **Verify the Setup:**

    - Use the connection string provided in the Atlas UI to connect to the cluster.
    
    - Verify that you can connect to the cluster and perform read/write operations.

## Summary:

In this lab, you learned how to deploy a MongoDB cluster on MongoDB Atlas, configure access, and verify the setup by connecting to the cluster. You can now use MongoDB Atlas to host your MongoDB databases in the cloud.