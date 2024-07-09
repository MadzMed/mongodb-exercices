# Monitoring MongoDB Atlas with mongostat and mongotop

## Objective:

Students will learn how to use mongostat and mongotop tools to monitor the performance of their MongoDB cluster on MongoDB Atlas.

## Prerequisites:

- MongoDB Atlas account with an active cluster
- MongoDB installed locally to use mongostat and mongotop

## Steps:

1. Deploy a Cluster on MongoDB Atlas:

    - Follow the account and cluster creation instructions available in the Introduction To Atlas.md document.

2. Configure Access to Your Cluster:

    - Create a database user and whitelist your IP address as described in the document.
    - Obtain the connection string for your cluster.

3. Use mongostat to Monitor Performance:

    - Open a terminal and connect to your cluster using mongostat with the connection string obtained.
    - Monitor real-time performance metrics like insert, query, update, delete operations, and more.

4. Use mongotop to Analyze Read and Write Times:

    - Open a terminal and connect to your cluster using mongotop with the connection string obtained.
    - Analyze the read and write times for the database operations.
    ( for this step, you need to run some queries on your cluster to see the results )

5. Report Observations:

    - Record the performance metrics observed using mongostat and mongotop.
    - Analyze the data to identify any performance bottlenecks or issues.
    - Share your findings with the class and discuss

## Expected Outcomes:

- Students should understand how to use mongostat and mongotop to monitor the performance of a MongoDB cluster.
- The report should include performance metrics analysis and recommendations for optimization if bottlenecks or anomalies are detected.

## Summary:

By using mongostat and mongotop, you can gain valuable insights into the performance of your MongoDB cluster on MongoDB Atlas. These tools provide real-time monitoring capabilities and help you identify and address any performance issues efficiently.
