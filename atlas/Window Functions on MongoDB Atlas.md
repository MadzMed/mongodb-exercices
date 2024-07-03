# Using Window Functions on MongoDB Atlas

In this tutorial, we will explore how to use window functions in MongoDB Atlas. Window functions allow you to perform calculations across a set of documents without grouping them into a single document. This can be useful for calculating running totals, moving averages, and other complex aggregations.

## Prerequisites

Before you begin, you will need the following:

- A MongoDB Atlas account
- A cluster deployed on MongoDB Atlas

## Steps

1. **Connect to Your Cluster:**

    - Log in to your MongoDB Atlas account.
    
    - Click on the "Clusters" tab in the left sidebar.
    
    - Click on the "Connect" button for the cluster you want to connect to.
    
    - Choose the connection method (e.g., MongoDB Shell, MongoDB Compass, etc.).
    
    - Follow the instructions to connect to the cluster using the selected method.

2. **Create a Sample Collection:**

 - Insert the following dataset into a collection named sales:

 ```javascript
 db.sales.insertMany([
  { "date": "2024-01-01", "amount": 100 },
  { "date": "2024-01-02", "amount": 200 },
  { "date": "2024-01-03", "amount": 150 },
  { "date": "2024-01-04", "amount": 300 },
  { "date": "2024-01-05", "amount": 250 }
])
```

3. **Calculate a Running Total:**

    - Use the `$sum` aggregation operator with the `$sum` window function to calculate a running total of the sales amounts.

    - The output will include the running total for each document in the collection.

4. **Calculate a Moving Average:**

    - Use the `$avg` aggregation operator with the `$avg` window function to calculate a moving average of the sales amounts.

    - The output will include the moving average for each document in the collection.

5. **Use Window Functions:**

    - Perform an aggregation query using the $setWindowFields stage to calculate a cumulative sales amount.

    - The output will include the cumulative sales amount for each document in the collection.

    ### Expected Output:

    ```json
    [
        { "_id": ObjectId("..."), "date": "2024-01-01", "amount": 100, "cumulativeSales": 100 },
        { "_id": ObjectId("..."), "date": "2024-01-02", "amount": 200, "cumulativeSales": 300 },
        { "_id": ObjectId("..."), "date": "2024-01-03", "amount": 150, "cumulativeSales": 450 },
        { "_id": ObjectId("..."), "date": "2024-01-04", "amount": 300, "cumulativeSales": 750 },
        { "_id": ObjectId("..."), "date": "2024-01-05", "amount": 250, "cumulativeSales": 1000 }
    ]
    ```

## Conclusion

In this tutorial, you learned how to use window functions in MongoDB Atlas to perform complex aggregations on your data. Window functions can be a powerful tool for calculating running totals, moving averages, and other aggregations across a set of documents. Experiment with different window functions to see how they can help you analyze and visualize your data in MongoDB Atlas.