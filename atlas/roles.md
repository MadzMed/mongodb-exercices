# Creating Role-Based Users in MongoDB Atlas

## Objective:

Students will learn how to create role-based users in MongoDB Atlas to manage database access and permissions effectively.

## Prerequisites:

- A MongoDB Atlas account
- A cluster deployed on MongoDB Atlas
- MongoDB command-line tools installed locally

## Steps:

1. **Access MongoDB Atlas:**

    - Go to the [MongoDB Atlas website](https://www.mongodb.com/cloud/atlas) and log in to your account.
    - Select the cluster for which you want to create a new user.

2. **Navigate to Database Access:**

    - Click on the "Database Access" tab in the left sidebar of the Atlas dashboard.
    - Click on the "Add New Database User" button.

3. **Create a New User:**

    - Enter the username and password for the new user.
    - Define the user's privileges by selecting the appropriate role from the dropdown menu.

4. **Assign Custom Roles:**

    - Navigate to "Project Settings" and select "Roles".
    - Click "Add New Role".
    - Enter a name for the role and specify the privileges (actions) it should include, such as find, insert, update, etc.

5. **Assign Roles to Users:**

    - Go back to the "Database Access" tab.
    - Edit the user you created earlier and assign the custom role you defined to the user.

6. **Test User Access:**

    - Use the MongoDB command-line tools to connect to your cluster with the new user credentials.
    - Verify that the user can perform the actions allowed by the assigned role.
    - Example Command:
        ```bash
        mongo "mongodb+srv://<username>:<password>@<cluster-url>/<database>"
        ```
    - Perform actions that are allowed by the assigned roles to ensure that the user has the correct permissions.

7. **Monitor User Activity:**

    - Check the "Logs" tab in the Atlas dashboard to monitor user activity and access logs.
    - Review the logs to ensure that users are accessing the database as expected and that there are no unauthorized activities.

## Report Observations:

- Document the process of creating users and assigning roles.
- Include screenshots and commands used during the process.
- Verify that the permissions are working as expected by performing various database operations.

## Expected Outcomes:

- Students should be able to create role-based users in MongoDB Atlas and assign custom roles to manage database access effectively.
- The report should detail the steps taken, any challenges faced, and verification of user permissions.

## Summary:

By creating role-based users in MongoDB Atlas, you can control access to your databases and ensure that users have the necessary permissions to perform their tasks. Custom roles allow you to define granular permissions based on specific actions, providing a secure and efficient way to manage database access in your MongoDB Atlas cluster.

